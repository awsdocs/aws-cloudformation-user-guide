# Create<a name="crpg-ref-requesttypes-create"></a>

Custom resource provider requests with `RequestType` set to `"Create"` are sent when the template developer creates a stack that contains a custom resource\.

## Request<a name="crpg-ref-requesttypes-create-request"></a>

Create requests contain the following fields:

RequestType  
Will be "Create"\.

RequestId  
A unique ID for the request\.

ResponseURL  
The response URL identifies a presigned S3 bucket that receives responses from the custom resource provider to AWS CloudFormation\.

ResourceType  
The template developer\-chosen resource type of the custom resource in the AWS CloudFormation template\. Custom resource type names can be up to 60 characters long and can include alphanumeric and the following characters: `_@-`\.

LogicalResourceId  
The template developer\-chosen name \(logical ID\) of the custom resource in the AWS CloudFormation template\. 

StackId  
The Amazon Resource Name \(ARN\) that identifies the stack that contains the custom resource\.

ResourceProperties  
This field contains the contents of the `Properties` object sent by the template developer\. Its contents are defined by the custom resource provider\.

### Example<a name="w7739ab1c27c24c17c19c11b5b6"></a>

```
{
   "RequestType" : "Create",
   "RequestId" : "unique id for this create request",
   "ResponseURL" : "pre-signed-url-for-create-response",
   "ResourceType" : "Custom::MyCustomResourceType",
   "LogicalResourceId" : "name of resource in template",
   "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid",
   "ResourceProperties" : {
      "key1" : "string",
      "key2" : [ "list" ],
      "key3" : { "key4" : "map" }
   }
}
```

## Responses<a name="crpg-ref-requesttypes-create-responses"></a>

### Success<a name="crpg-ref-requesttypes-create-responses-success"></a>

When the create request is successful, a response must be sent to the S3 bucket with the following fields:

Status  
Must be "SUCCESS"\.

RequestId  
A unique ID for the request\. This response value should be copied *verbatim* from the request\.

LogicalResourceId  
The template developer\-chosen name \(logical ID\) of the custom resource in the AWS CloudFormation template\. This response value should be copied *verbatim* from the request\.

StackId  
The Amazon Resource Name \(ARN\) that identifies the stack that contains the custom resource\. This response value should be copied *verbatim* from the request\.

PhysicalResourceId  
This value should be an identifier unique to the custom resource vendor, and can be up to 1 Kb in size\. The value must be a non\-empty string and must be identical for all responses for the same resource\.

NoEcho  
Optional\. Indicates whether to mask the output of the custom resource when retrieved by using the `Fn::GetAtt` function\. If set to `true`, all returned values are masked with asterisks \(\*\*\*\*\*\), *except for those stored in the `Metadata` section of the template*\. CloudFormation does not transform, modify, or redact any information you include in the `Metadata` section\. The default value is `false`\.  
For more information about using `NoEcho` to mask sensitive information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

Data  
Optional\. The custom resource provider\-defined name\-value pairs to send with the response\. You can access the values provided here by name in the template with `Fn::GetAtt`\.  
If the name\-value pairs contain sensitive information, you should use the `NoEcho` field to mask the output of the custom resource\. Otherwise, the values are visible through APIs that surface property values \(such as `DescribeStackEvents`\)\.

#### Example<a name="w7739ab1c27c24c17c19c11b7b2b6"></a>

```
{
   "Status" : "SUCCESS",
   "RequestId" : "unique id for this create request (copied from request)",
   "LogicalResourceId" : "name of resource in template (copied from request)",
   "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid (copied from request)",
   "PhysicalResourceId" : "required vendor-defined physical id that is unique for that vendor",
   "Data" : {
      "keyThatCanBeUsedInGetAtt1" : "data for key 1",
      "keyThatCanBeUsedInGetAtt2" : "data for key 2"
   }
}
```

### Failed<a name="crpg-ref-requesttypes-create-responses-failed"></a>

When the create request fails, a response must be sent to the S3 bucket with the following fields:

Status  
Must be "FAILED"\.

Reason  
Describes the reason for a failure response\.

RequestId  
A unique ID for the request\. This response value should be copied *verbatim* from the request\.

LogicalResourceId  
The template developer\-chosen name \(logical ID\) of the custom resource in the AWS CloudFormation template\. This response value should be copied *verbatim* from the request\.

StackId  
The Amazon Resource Name \(ARN\) that identifies the stack that contains the custom resource\. This response value should be copied *verbatim* from the request\.

PhysicalResourceId  
This value should be an identifier unique to the custom resource vendor, and can be up to 1 Kb in size\. The value must be a non\-empty string and must be identical for all responses for the same resource\.

#### Example<a name="w7739ab1c27c24c17c19c11b7b4b6"></a>

```
{
   "Status" : "FAILED",
   "Reason" : "Required failure reason string",
   "RequestId" : "unique id for this create request (copied from request)",
   "LogicalResourceId" : "name of resource in template (copied from request)",
   "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid (copied from request)",
   "PhysicalResourceId" : "required vendor-defined physical id that is unique for that vendor"
}
```