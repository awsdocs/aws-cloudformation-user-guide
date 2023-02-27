# AWS::S3Outposts::Bucket Rule<a name="aws-properties-s3outposts-bucket-rule"></a>

A container for an Amazon S3 on Outposts bucket lifecycle rule\.

## Syntax<a name="aws-properties-s3outposts-bucket-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3outposts-bucket-rule-syntax.json"></a>

```
{
  "[AbortIncompleteMultipartUpload](#cfn-s3outposts-bucket-rule-abortincompletemultipartupload)" : AbortIncompleteMultipartUpload,
  "[ExpirationDate](#cfn-s3outposts-bucket-rule-expirationdate)" : String,
  "[ExpirationInDays](#cfn-s3outposts-bucket-rule-expirationindays)" : Integer,
  "[Filter](#cfn-s3outposts-bucket-rule-filter)" : Filter,
  "[Id](#cfn-s3outposts-bucket-rule-id)" : String,
  "[Status](#cfn-s3outposts-bucket-rule-status)" : String
}
```

### YAML<a name="aws-properties-s3outposts-bucket-rule-syntax.yaml"></a>

```
  [AbortIncompleteMultipartUpload](#cfn-s3outposts-bucket-rule-abortincompletemultipartupload): 
    AbortIncompleteMultipartUpload
  [ExpirationDate](#cfn-s3outposts-bucket-rule-expirationdate): String
  [ExpirationInDays](#cfn-s3outposts-bucket-rule-expirationindays): Integer
  [Filter](#cfn-s3outposts-bucket-rule-filter): 
    Filter
  [Id](#cfn-s3outposts-bucket-rule-id): String
  [Status](#cfn-s3outposts-bucket-rule-status): String
```

## Properties<a name="aws-properties-s3outposts-bucket-rule-properties"></a>

`AbortIncompleteMultipartUpload`  <a name="cfn-s3outposts-bucket-rule-abortincompletemultipartupload"></a>
The container for the abort incomplete multipart upload rule\.  
*Required*: No  
*Type*: [AbortIncompleteMultipartUpload](aws-properties-s3outposts-bucket-abortincompletemultipartupload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpirationDate`  <a name="cfn-s3outposts-bucket-rule-expirationdate"></a>
Specifies the expiration for the lifecycle of the object by specifying an expiry date\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpirationInDays`  <a name="cfn-s3outposts-bucket-rule-expirationindays"></a>
Specifies the expiration for the lifecycle of the object in the form of days that the object has been in the S3 on Outposts bucket\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filter`  <a name="cfn-s3outposts-bucket-rule-filter"></a>
The container for the filter of the lifecycle rule\.  
*Required*: No  
*Type*: [Filter](aws-properties-s3outposts-bucket-filter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-s3outposts-bucket-rule-id"></a>
 The unique identifier for the lifecycle rule\. The value can't be longer than 255 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-s3outposts-bucket-rule-status"></a>
If `Enabled`, the rule is currently being applied\. If `Disabled`, the rule is not currently being applied\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)