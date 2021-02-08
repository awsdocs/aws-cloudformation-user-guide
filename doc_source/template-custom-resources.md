# Custom resources<a name="template-custom-resources"></a>

Custom resources enable you to write custom provisioning logic in templates that AWS CloudFormation runs anytime you create, update \(if you changed the custom resource\), or delete stacks\. For example, you might want to include resources that aren't available as AWS CloudFormation [resource types](aws-template-resource-type-ref.md)\. You can include those resources by using custom resources\. That way you can still manage all your related resources in a single stack\.

Use the [AWS::CloudFormation::CustomResource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cfn-customresource.html) or [Custom::*MyCustomResourceTypeName*](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cfn-customresource.html#aws-resource-cfn-customresource--remarks) resource type to define custom resources in your templates\. Custom resources require one property: the service token, which specifies where AWS CloudFormation sends requests to, such as an Amazon SNS topic\.

**Note**  
If you use the [VPC endpoint](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html) feature, custom resources in the VPC must have access to AWS CloudFormation\-specific S3 buckets\. Custom resources must send responses to a pre\-signed Amazon S3 URL\. If they can't send responses to Amazon S3, AWS CloudFormation won't receive a response and the stack operation fails\. For more information, see [Setting up VPC endpoints for AWS CloudFormation](cfn-vpce-bucketnames.md)\.

## How custom resources work<a name="how-custom-resources-work"></a>

Any action taken for a custom resource involves three parties\.

template developer  
Creates a template that includes a custom resource type\. The template developer specifies the service token and any input data in the template\.

custom resource provider  
Owns the custom resource and determines how to handle and respond to requests from AWS CloudFormation\. The custom resource provider must provide a service token that the template developer uses\.

AWS CloudFormation  
During a stack operation, sends a request to a service token that is specified in the template, and then waits for a response before proceeding with the stack operation\.

 The template developer and custom resource provider can be the same person or entity, but the process is the same\. The following steps describe the general process:

1. The template developer defines a custom resource in their template, which includes a service token and any input data parameters\. Depending on the custom resource, the input data might be required; however, the service token is always required\.

   The service token specifies where AWS CloudFormation sends requests to, such as to an Amazon SNS topic ARN or to an AWS Lambda function ARN\. For more information, see [AWS::CloudFormation::CustomResource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cfn-customresource.html)\. The service token and the structure of the input data is defined by the custom resource provider\.

1. Whenever anyone uses the template to create, update, or delete a custom resource, AWS CloudFormation sends a request to the specified service token\. The service token must be in the same region in which you are creating the stack\.

   In the request, AWS CloudFormation includes information such as the request type and a pre\-signed Amazon Simple Storage Service URL, where the custom resource sends responses to\. For more information about what's included in the request, see [Custom resource request objects](crpg-ref-requests.md)\.

   The following sample data shows what AWS CloudFormation includes in a request:

   ```
   {
      "RequestType" : "Create",
      "ResponseURL" : "http://pre-signed-S3-url-for-response",
      "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
      "RequestId" : "unique id for this create request",
      "ResourceType" : "Custom::TestResource",
      "LogicalResourceId" : "MyTestResource",
      "ResourceProperties" : {
         "Name" : "Value",
         "List" : [ "1", "2", "3" ]
      }
   }
   ```
**Note**  
In this example, `ResourceProperties` allows AWS CloudFormation to create a custom payload to send to the Lambda function\.

1. The custom resource provider processes the AWS CloudFormation request and returns a response of `SUCCESS` or `FAILED` to the pre\-signed URL\. The custom resource provider provides the response in a JSON\-formatted file and uploads it to the pre\-signed S3 URL\. For more information, see [Uploading objects using pre\-signed URLs](https://docs.aws.amazon.com/AmazonS3/latest/dev/PresignedUrlUploadObject.html) in the *Amazon Simple Storage Service Developer Guide*\.

   In the response, the custom resource provider can also include name\-value pairs that the template developer can access\. For example, the response can include output data if the request succeeded or an error message if the request failed\. For more information about responses, see [Custom resource response objects](crpg-ref-responses.md)\.
**Important**  
If the name\-value pairs contain sensitive information, you should use the `NoEcho` field to mask the output of the custom resource\. Otherwise, the values are visible through APIs that surface property values \(such as `DescribeStackEvents`\)\.  
For more information about using `NoEcho` to mask sensitive information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

   The custom resource provider is responsible for listening and responding to the request\. For example, for Amazon SNS notifications, the custom resource provider must listen and respond to notifications that are sent to a specific topic ARN\. AWS CloudFormation waits and listens for a response in the pre\-signed URL location\.

   The following sample data shows what a custom resource might include in a response:

   ```
   {
      "Status" : "SUCCESS",
      "PhysicalResourceId" : "TestResource1",
      "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/stack-name/guid",
      "RequestId" : "unique id for this create request",
      "LogicalResourceId" : "MyTestResource",
      "Data" : {
         "OutputName1" : "Value1",
         "OutputName2" : "Value2",
      }
   }
   ```

1. After getting a `SUCCESS` response, AWS CloudFormation proceeds with the stack operation\. If a `FAILED` response or no response is returned, the operation fails\. Any output data from the custom resource is stored in the pre\-signed URL location\. The template developer can retrieve that data by using the [`Fn::GetAtt`](intrinsic-function-reference-getatt.md) function\.