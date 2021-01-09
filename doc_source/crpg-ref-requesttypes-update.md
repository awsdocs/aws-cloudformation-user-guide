# Update<a name="crpg-ref-requesttypes-update"></a>

Custom resource provider requests with `RequestType` set to `"Update"` are sent when there's any change to the properties of the custom resource within the template\. Therefore, custom resource code doesn't have to detect changes because it knows that its properties have changed when Update is being called\.

## Request<a name="crpg-ref-requesttypes-update-request"></a>

Update requests contain the following fields:

RequestType  
Will be "Update"\.

RequestId  
A unique ID for the request\.

ResponseURL  
The response URL identifies a presigned S3 bucket that receives responses from the custom resource provider to AWS CloudFormation\.

ResourceType  
The template developer\-chosen resource type of the custom resource in the AWS CloudFormation template\. Custom resource type names can be up to 60 characters long and can include alphanumeric and the following characters: `_@-`\. You can't change the type during an update\.

LogicalResourceId  
The template developer\-chosen name \(logical ID\) of the custom resource in the AWS CloudFormation template\. 

StackId  
The Amazon Resource Name \(ARN\) that identifies the stack that contains the custom resource\.

PhysicalResourceId  
A required custom resource provider\-defined physical ID that is unique for that provider\.

ResourceProperties  
The new resource property values that are declared by the template developer in the updated AWS CloudFormation template\.

OldResourceProperties  
The resource property values that were previously declared by the template developer in the AWS CloudFormation template\.

### Example<a name="w7739ab1c27c24c17c19c16b5b6"></a>

```
{
   "RequestType" : "Update",
   "RequestId" : "unique id for this update request",
   "ResponseURL" : "pre-signed-url-for-update-response",
   "ResourceType" : "Custom::MyCustomResourceType",
   "LogicalResourceId" : "name of resource in template",
   "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid",
   "PhysicalResourceId" : "custom resource provider-defined physical id",
   "ResourceProperties" : {
      "key1" : "new-string",
      "key2" : [ "new-list" ],
      "key3" : { "key4" : "new-map" }
   },
   "OldResourceProperties" : {
      "key1" : "string",
      "key2" : [ "list" ],
      "key3" : { "key4" : "map" }
   }
}
```

## Responses<a name="crpg-ref-requesttypes-responses"></a>

### Success<a name="crpg-ref-requesttypes-responses-success"></a>

If the custom resource provider is able to successfully update the resource, AWS CloudFormation expects the status to be set to `"SUCCESS"` in the response\.

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

#### Example<a name="w7739ab1c27c24c17c19c16b7b2b6"></a>

```
{
   "Status" : "SUCCESS",
   "RequestId" : "unique id for this update request (copied from request)",
   "LogicalResourceId" : "name of resource in template (copied from request)",
   "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid (copied from request)",
   "PhysicalResourceId" : "custom resource provider-defined physical id",
   "Data" : {
      "keyThatCanBeUsedInGetAtt1" : "data for key 1",
      "keyThatCanBeUsedInGetAtt2" : "data for key 2"
   }
}
```

### Failed<a name="crpg-ref-requesttypes-responses-failed"></a>

If the resource can't be updated with a new set of properties, AWS CloudFormation expects the status to be set to "FAILED", along with a failure reason in the response\.

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

#### Example<a name="w7739ab1c27c24c17c19c16b7b4b6"></a>

```
{
   "Status" : "FAILED",
   "Reason" : "Required failure reason string",
   "RequestId" : "unique id for this update request (copied from request)",
   "LogicalResourceId" : "name of resource in template (copied from request)",
   "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid (copied from request)",
   "PhysicalResourceId" : "custom resource provider-defined physical id"
}
```