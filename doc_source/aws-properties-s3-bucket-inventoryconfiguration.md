# Amazon S3 Bucket InventoryConfiguration<a name="aws-properties-s3-bucket-inventoryconfiguration"></a>

<a name="aws-properties-s3-bucket-inventoryconfiguration-description"></a>The `InventoryConfiguration` property type specifies the inventory configuration for an Amazon S3 bucket\.

For more information, see [GET Bucket inventory](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketGETInventoryConfig.html) in the *Amazon Simple Storage Service API Reference*

<a name="aws-properties-s3-bucket-inventoryconfiguration-inheritance"></a> `InventoryConfiguration` is a property of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) resource type\. 

## Syntax<a name="aws-properties-s3-bucket-inventoryconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-inventoryconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-destination)" : Destination,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-enabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-id)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-includedobjectversions)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-optionalfields)" : [ String, ... ]
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-prefix)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-schedulefrequency)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-inventoryconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-destination): Destination
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-enabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-id): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-includedobjectversions): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-optionalfields): 
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-prefix): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-inventoryconfiguration-schedulefrequency): String
```

## Properties<a name="aws-properties-s3-bucket-inventoryconfiguration-properties"></a>

`Destination`  
Information about where to publish the inventory results\.  
 *Required*: Yes  
 *Type*: [Amazon S3 Bucket Destination](aws-properties-s3-bucket-destination.md)  
 *Update requires*: No interruption 

`Enabled`  
Specifies whether the inventory is enabled or disabled\. If set to `True`, an inventory list is generated\. If set to `False`, no inventory list is generated\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Id`  
The ID that identifies the inventory configuration\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`IncludedObjectVersions`  
Object versions to include in the inventory list\. If set to `All`, the list includes all the object versions, which adds the version related fields `VersionId`, `IsLatest`, and `DeleteMarker` to the list\. If set to `Current`, the list does not contain these version related fields\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`OptionalFields`  
The optional fields that are included in the inventory results\.  
 *Required*: No  
 *Type*: StringList  
 *Update requires*: No interruption 

`Prefix`  
The prefix that is prepended to all inventory results\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ScheduleFrequency`  
The frequency of inventory results generation\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 