# AWS::CloudFormation::CustomResource<a name="aws-resource-cfn-customresource"></a>

In a CloudFormation template, you use the `AWS::CloudFormation::CustomResource` or `Custom::String ` resource type to specify custom resources\.

Custom resources provide a way for you to write custom provisioning logic in CloudFormation template and have CloudFormation run it during a stack operation, such as when you create, update or delete a stack\. For more information, see [Custom Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-custom-resources.html)\.

**Note**  
If you use the [VPC Endpoints](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html) feature, custom resources in the VPC must have access to CloudFormation\-specific Amazon Simple Storage Service \(Amazon S3\) buckets\. Custom resources must send responses to a pre\-signed Amazon S3 URL\. If they can't send responses to Amazon S3, CloudFormation won't receive a response and the stack operation fails\. For more information, see [Setting Up VPC Endpoints for AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-vpce-bucketnames.html)\.

## Syntax<a name="aws-resource-cfn-customresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cfn-customresource-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::CustomResource",
  "Properties" : {
      "[ServiceToken](#cfn-customresource-servicetoken)" : String
    }
}
```

### YAML<a name="aws-resource-cfn-customresource-syntax.yaml"></a>

```
Type: AWS::CloudFormation::CustomResource
Properties: 
  [ServiceToken](#cfn-customresource-servicetoken): String
```

## Properties<a name="aws-resource-cfn-customresource-properties"></a>

`ServiceToken`  <a name="cfn-customresource-servicetoken"></a>
Only one property is defined by AWS for a custom resource: `ServiceToken`\. All other properties are defined by the service provider\.
The service token that was given to the template developer by the service provider to access the service, such as an Amazon SNS topic ARN or Lambda function ARN\. The service token must be from the same region in which you are creating the stack\.  
Updates are not supported\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Remarks<a name="aws-resource-cfn-customresource--remarks"></a>

 *Specifying Custom Resource Type Names* 

For custom resources, you can specify `AWS::CloudFormation::CustomResource` as the resource type, or you can specify your own resource type name\. For example, instead of using `AWS::CloudFormation::CustomResource`, you can use `Custom::MyCustomResourceTypeName`\.

Custom resource type names can include alphanumeric characters and the following characters: `_@-`\. You can specify a custom resource type name up to a maximum length of 60 characters\. You cannot change the type during an update\.

Using your own resource type names helps you quickly differentiate the types of custom resources in your stack\. For example, if you had two custom resources that conduct two different ping tests, you could name their type as `Custom::PingTester` to make them easily identifiable as ping testers \(instead of using `AWS::CloudFormation::CustomResource`\)\.

 *Replacing a Custom Resource During an Update* 

You can update custom resources that require a replacement of the underlying physical resource\. When you update a custom resource in a CloudFormation template, CloudFormation sends an update request to that custom resource\. If the custom resource requires a replacement, the new custom resource must send a response with the new physical ID\. When CloudFormation receives the response, it compares the `PhysicalResourceId` between the old and new custom resources\. If they are different, CloudFormation recognizes the update as a replacement and sends a delete request to the old resource\. For a step\-by\-step walkthrough of this process, see [Stack Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/crpg-walkthrough-stack-updates.html)\. 

Note the following: 
+ You can monitor the progress of the update in the Events tab\. For more information, see [Viewing Stack Data and Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-view-stack-data-resources.html)\.
+ For more information about resource behavior during updates, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.

 *Retrieving Return Values* 

For a custom resource, return values are defined by the custom resource provider, and are retrieved by calling Fn::GetAtt on the provider\-defined attributes\.

## Examples<a name="aws-resource-cfn-customresource--examples"></a>

### Creating a Custom Resource Definition in a Template<a name="aws-resource-cfn-customresource--examples--Creating_a_Custom_Resource_Definition_in_a_Template"></a>

The following example demonstrates how to create a custom resource definition in a template\.

All properties other than `ServiceToken`, and all `Fn::GetAtt` resource attributes, are defined by the custom resource provider\.

#### JSON<a name="aws-resource-cfn-customresource--examples--Creating_a_Custom_Resource_Definition_in_a_Template--json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "MyFrontEndTest" : {
      "Type": "Custom::PingTester",
      "Version" : "1.0",
      "Properties" : {
        "ServiceToken": "arn:aws:sns:us-east-1:84969EXAMPLE:CRTest",
        "key1" : "string",
        "key2" : [ "list" ],
        "key3" : { "key4" : "map" }
      }
    }
  },
  "Outputs" : {
    "CustomResourceAttribute1" : {
      "Value" : { "Fn::GetAtt" : ["MyFrontEndTest", "responseKey1"] }
    },
    "CustomResourceAttribute2" : {
      "Value" : { "Fn::GetAtt" : ["MyFrontEndTest", "responseKey2"] }
    }
  }
}
```

#### YAML<a name="aws-resource-cfn-customresource--examples--Creating_a_Custom_Resource_Definition_in_a_Template--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  MyFrontEndTest: 
    Type: "Custom::PingTester"
    Version: "1.0"
    Properties: 
      ServiceToken: "arn:aws:sns:us-east-1:84969EXAMPLE:CRTest"
      key1: string
      key2: 
        - list
      key3: 
        key4: map
Outputs: 
  CustomResourceAttribute1: 
    Value: 
      Fn::GetAtt: 
        - MyFrontEndTest
        - responseKey1
  CustomResourceAttribute2: 
    Value: 
      Fn::GetAtt: 
        - MyFrontEndTest
        - responseKey2
```

### Using an AWS Lambda Function in a Custom Resource<a name="aws-resource-cfn-customresource--examples--Using_an_AWS_Lambda_Function_in_a_Custom_Resource"></a>

With Lambda functions and custom resources, you can run custom code in response to stack events \(create, update, and delete\)\. The following custom resource invokes a Lambda function and sends it the StackName property as input\. The function uses this property to get outputs from the appropriate stack\.

#### JSON<a name="aws-resource-cfn-customresource--examples--Using_an_AWS_Lambda_Function_in_a_Custom_Resource--json"></a>

```
"MyCustomResource" : {
  "Type" : "Custom::TestLambdaCrossStackRef",
  "Properties" : {
    "ServiceToken": { "Fn::Join": [ "", [ "arn:aws:lambda:", { "Ref": "AWS::Region" }, ":", { "Ref": "AWS::AccountId" }, ":function:", {"Ref" : "LambdaFunctionName"} ] ] },
    "StackName": {
      "Ref": "NetworkStackName"
    }
  }
}
```

#### YAML<a name="aws-resource-cfn-customresource--examples--Using_an_AWS_Lambda_Function_in_a_Custom_Resource--yaml"></a>

```
MyCustomResource: 
  Type: "Custom::TestLambdaCrossStackRef"
  Properties: 
    ServiceToken:
      !Sub arn:aws:lambda:${AWS::Region}:${AWS::AccountId}:function:${LambdaFunctionName}
    StackName: 
      Ref: "NetworkStackName"
```