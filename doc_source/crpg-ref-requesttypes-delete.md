# Delete<a name="crpg-ref-requesttypes-delete"></a>

Custom resource provider requests with `RequestType` set to `"Delete"` are sent when the template developer deletes a stack that contains a custom resource\. To successfully delete a stack with a custom resource, the custom resource provider must respond successfully to a delete request\.

## Request<a name="crpg-ref-requesttypes-delete-request"></a>

Delete requests contain the following fields:

RequestType  
Will be "Delete"\.

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

PhysicalResourceId  
A required custom resource provider\-defined physical ID that is unique for that provider\.

ResourceProperties  
This field contains the contents of the `Properties` object sent by the template developer\. Its contents are defined by the custom resource provider\.

### Example<a name="w7739ab1c27c24c17c19c14b5b6"></a>

```
{
   "RequestType" : "Delete",
   "RequestId" : "unique id for this delete request",
   "ResponseURL" : "pre-signed-url-for-delete-response",
   "ResourceType" : "Custom::MyCustomResourceType",
   "LogicalResourceId" : "name of resource in template",
   "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid",
   "PhysicalResourceId" : "custom resource provider-defined physical id",
   "ResourceProperties" : {
      "key1" : "string",
      "key2" : [ "list" ],
      "key3" : { "key4" : "map" }
   }
}
```

## Responses<a name="crpg-ref-requesttypes-delete-responses"></a>

### Success<a name="crpg-ref-requesttypes-delete-responses-success"></a>

When the delete request is successful, a response must be sent to the S3 bucket with the following fields:

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

#### Example<a name="w7739ab1c27c24c17c19c14b7b2b6"></a>

```
{
   "Status" : "SUCCESS",
   "RequestId" : "unique id for this delete request (copied from request)",
   "LogicalResourceId" : "name of resource in template (copied from request)",
   "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid (copied from request)",
   "PhysicalResourceId" : "custom resource provider-defined physical id"
}
```

### Failed<a name="crpg-ref-requesttypes-delete-responses-failed"></a>

When the delete request fails, a response must be sent to the S3 bucket with the following fields:

Status  
Must be "FAILED"\.

Reason  
The reason for the failure\.

RequestId  
The `RequestId` value copied from the [delete request](#crpg-ref-requesttypes-delete-request)\.

LogicalResourceId  
The `LogicalResourceId` value copied from the [delete request](#crpg-ref-requesttypes-delete-request)\.

StackId  
The `StackId` value copied from the [delete request](#crpg-ref-requesttypes-delete-request)\.

PhysicalResourceId  
A required custom resource provider\-defined physical ID that is unique for that provider\.

#### Example<a name="w7739ab1c27c24c17c19c14b7b4b6"></a>

```
{
  "Status" : "FAILED",
  "Reason" : "Required failure reason string",
  "RequestId" : "unique id for this delete request (copied from request)",
  "LogicalResourceId" : "name of resource in template (copied from request)",
  "StackId" : "arn:aws:cloudformation:us-east-2:namespace:stack/stack-name/guid (copied from request)",
  "PhysicalResourceId" : "custom resource provider-defined physical id"
}
```