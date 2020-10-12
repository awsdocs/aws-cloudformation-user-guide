# AWS::S3::Bucket S3KeyFilter<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key"></a>

A container for object key name prefix and suffix filtering rules\.

**Note**  
The same type of filter rule cannot be used more than once\. For example, you cannot specify two prefix rules\.

## Syntax<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-syntax.json"></a>

```
{
  "[Rules](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules)" : [ FilterRule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-syntax.yaml"></a>

```
  [Rules](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules): 
    - FilterRule
```

## Properties<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-properties"></a>

`Rules`  <a name="cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules"></a>
A list of containers for the key\-value pair that defines the criteria for the filter rule\.  
*Required*: Yes  
*Type*: List of [FilterRule](aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-rules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)