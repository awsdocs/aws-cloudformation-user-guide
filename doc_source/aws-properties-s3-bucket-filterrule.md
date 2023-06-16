# AWS::S3::Bucket FilterRule<a name="aws-properties-s3-bucket-filterrule"></a>

Specifies the Amazon S3 object key name to filter on and whether to filter on the suffix or prefix of the key name\.

## Syntax<a name="aws-properties-s3-bucket-filterrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-filterrule-syntax.json"></a>

```
{
  "[Name](#cfn-s3-bucket-filterrule-name)" : String,
  "[Value](#cfn-s3-bucket-filterrule-value)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-filterrule-syntax.yaml"></a>

```
  [Name](#cfn-s3-bucket-filterrule-name): String
  [Value](#cfn-s3-bucket-filterrule-value): String
```

## Properties<a name="aws-properties-s3-bucket-filterrule-properties"></a>

`Name`  <a name="cfn-s3-bucket-filterrule-name"></a>
The object key name prefix or suffix identifying one or more objects to which the filtering rule applies\. The maximum length is 1,024 characters\. Overlapping prefixes and suffixes are not supported\. For more information, see [Configuring Event Notifications](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon S3 User Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `prefix | suffix`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-s3-bucket-filterrule-value"></a>
The value that the filter searches for in object key names\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)