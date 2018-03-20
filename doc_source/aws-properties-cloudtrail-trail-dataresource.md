# AWS CloudTrail Trail DataResource<a name="aws-properties-cloudtrail-trail-dataresource"></a>

The `DataResource` property type specifies Amazon S3 objects for event selectors in a CloudTrail trail\. Data events are object\-level API operations that access Amazon S3 objects, such as `GetObject`, `DeleteObject`, and `PutObject`\. You can specify up to 250 Amazon S3 buckets and object prefixes for a trail\. For more information, see [DataResource](http://docs.aws.amazon.com/awscloudtrail/latest/APIReference/API_DataResource.html) in the *AWS CloudTrail API Reference*\.

 `DataResource` is a property of the [CloudTrail Trail EventSelector](aws-properties-cloudtrail-trail-eventselector.md) property type\. 

## Syntax<a name="aws-properties-cloudtrail-trail-dataresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudtrail-trail-dataresource-syntax.json"></a>

```
{
  "[Type](#cfn-cloudtrail-trail-dataresource-type)" : String,
  "[Values](#cfn-cloudtrail-trail-dataresource-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudtrail-trail-dataresource-syntax.yaml"></a>

```
[Type](#cfn-cloudtrail-trail-dataresource-type): String
[Values](#cfn-cloudtrail-trail-dataresource-values): 
  - String
```

## Properties<a name="aws-properties-cloudtrail-trail-dataresource-properties"></a>

`Type`  <a name="cfn-cloudtrail-trail-dataresource-type"></a>
The resource type to log data events for\. You can specify only the following value: `AWS::S3::Object`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Values`  <a name="cfn-cloudtrail-trail-dataresource-values"></a>
A list of ARN\-like strings for the specified Amazon S3 objects\.  
To log data events for all objects in all Amazon S3 buckets in your AWS account, specify the prefix as `arn:aws:s3:::`\.  
To log data events for all objects in an Amazon S3 bucket, specify the bucket and an empty object prefix such as `arn:aws:s3:::bucket-1/`\. The trail logs data events for all objects in this Amazon S3 bucket\.  
To log data events for specific objects, specify the Amazon S3 bucket and object prefix such as `arn:aws:s3:::bucket-1/example-images`\. The trail logs data events for objects in the bucket that match the prefix\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 