# Custom resource request objects<a name="crpg-ref-requests"></a>

## Template developer request properties<a name="crpg-ref-request-properties"></a>

The template developer uses the AWS CloudFormation resource, [AWS::CloudFormation::CustomResource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cfn-customresource.html), to specify a custom resource in a template\.

In `AWS::CloudFormation::CustomResource`, all properties are defined by the custom resource provider\. There is only one required property: `ServiceToken`\.

ServiceToken  <a name="crpg-ref-request-servicetoken"></a>
The service token \(an Amazon SNS topic or AWS Lambda function Amazon Resource Name\) that is obtained from the custom resource provider to access the service\. The service token must be in the same region in which you are creating the stack\.  
*Required*: Yes  
*Type*: String

All other fields in the resource properties are optional and are sent, verbatim, to the custom resource provider in the request's `ResourceProperties` field\. The provider defines both the names and the valid contents of these fields\.

## Custom resource provider request fields<a name="crpg-ref-request-fields"></a>

These fields are sent in JSON requests from AWS CloudFormation to the custom resource provider in the SNS topic that the provider has configured for this purpose\.

RequestType  <a name="crpg-ref-request-requesttype"></a>
The request type is set by the AWS CloudFormation stack operation \(create\-stack, update\-stack, or delete\-stack\) that was initiated by the template developer for the stack that contains the custom resource\.  
Must be one of: `Create`, `Update`, or `Delete`\. For more information, see [Custom resource request types](crpg-ref-requesttypes.md)\.  
*Required*: Yes  
*Type*: String

ResponseURL  <a name="crpg-ref-request-responseurl"></a>
The response URL identifies a presigned S3 bucket that receives responses from the custom resource provider to AWS CloudFormation\.  
*Required*: Yes  
*Type*: String

StackId  <a name="crpg-ref-request-stackid"></a>
The Amazon Resource Name \(ARN\) that identifies the stack that contains the custom resource\.  
Combining the `StackId` with the `RequestId` forms a value that you can use to uniquely identify a request on a particular custom resource\.  
*Required*: Yes  
*Type*: String

RequestId  <a name="crpg-ref-request-requestid"></a>
A unique ID for the request\.  
Combining the `StackId` with the `RequestId` forms a value that you can use to uniquely identify a request on a particular custom resource\.  
*Required*: Yes  
*Type*: String

ResourceType  <a name="crpg-ref-request-resourcetype"></a>
The template developer\-chosen resource type of the custom resource in the AWS CloudFormation template\. Custom resource type names can be up to 60 characters long and can include alphanumeric and the following characters: `_@-`\.  
*Required*: Yes  
*Type*: String

LogicalResourceId  <a name="crpg-ref-request-logicalresourceid"></a>
The template developer\-chosen name \(logical ID\) of the custom resource in the AWS CloudFormation template\. This is provided to facilitate communication between the custom resource provider and the template developer\.  
*Required*: Yes  
*Type*: String

PhysicalResourceId  <a name="crpg-ref-request-physicalresourceid"></a>
A required custom resource provider\-defined physical ID that is unique for that provider\.  
*Required*: Always sent with `Update` and `Delete` requests; never sent with `Create`\.  
*Type*: String

ResourceProperties  <a name="crpg-ref-request-resourceproperties"></a>
This field contains the contents of the `Properties` object sent by the template developer\. Its contents are defined by the custom resource provider\.  
*Required*: No  
*Type*: JSON object

OldResourceProperties  <a name="crpg-ref-request-oldresourceproperties"></a>
Used only for `Update` requests\. Contains the resource properties that were declared previous to the update request\.  
*Required*: Yes  
*Type*: JSON object