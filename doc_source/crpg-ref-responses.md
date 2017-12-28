# Custom Resource Response Objects<a name="crpg-ref-responses"></a>

## Custom Resource Provider Response Fields<a name="crpg-ref-responses-fields"></a>

The following are properties that the custom resource provider includes when it sends the JSON file to the presigned URL\. For more information about uploading objects by using presigned URLs, see the related [topic](http://docs.aws.amazon.com/AmazonS3/latest/dev/PresignedUrlUploadObject.html) in the *Amazon Simple Storage Service Developer Guide*\.

Status  
The status value sent by the custom resource provider in response to an AWS CloudFormation\-generated request\.  
Must be either `SUCCESS` or `FAILED`\.  
*Required: *Yes  
*Type*: String

Reason  
Describes the reason for a failure response\.  
*Required:* Required if `Status` is `FAILED`\. It's optional otherwise\.  
*Type*: String

PhysicalResourceId  
This value should be an identifier unique to the custom resource vendor, and can be up to 1 Kb in size\. The value must be a non\-empty string and must be identical for all responses for the same resource\.  
*Required: *Yes  
*Type*: String

StackId  
The Amazon Resource Name \(ARN\) that identifies the stack that contains the custom resource\. This response value should be copied *verbatim* from the request\.  
*Required: *Yes  
*Type*: String

RequestId  
A unique ID for the request\. This response value should be copied *verbatim* from the request\.  
*Required: *Yes  
*Type*: String

LogicalResourceId  
The template developer\-chosen name \(logical ID\) of the custom resource in the AWS CloudFormation template\. This response value should be copied *verbatim* from the request\.  
*Required: *Yes  
*Type*: String

NoEcho  
Optional\. Indicates whether to mask the output of the custom resource when retrieved by using the `Fn::GetAtt` function\. If set to `true`, all returned values are masked with asterisks \(\*\*\*\*\*\)\. The default value is `false`\.  
*Required: *No  
*Type*: Boolean

Data  
Optional\. The custom resource provider\-defined name\-value pairs to send with the response\. You can access the values provided here by name in the template with `Fn::GetAtt`\.  
If the name\-value pairs contain sensitive information, you should use the `NoEcho` field to mask the output of the custom resource\. Otherwise, the values are visible through APIs that surface property values \(such as `DescribeStackEvents`\)\.
*Required: *No  
*Type*: JSON object