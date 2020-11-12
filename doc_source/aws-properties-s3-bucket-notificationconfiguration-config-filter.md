# AWS::S3::Bucket NotificationFilter<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter"></a>

Specifies object key name filtering rules\. For information about key name filtering, see [Configuring Event Notifications](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon Simple Storage Service Developer Guide*\.

## Syntax<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-syntax.json"></a>

```
{
  "[S3Key](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key)" : S3KeyFilter
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-syntax.yaml"></a>

```
  [S3Key](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key): 
    S3KeyFilter
```

## Properties<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-properties"></a>

`S3Key`  <a name="cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key"></a>
A container for object key name prefix and suffix filtering rules\.  
*Required*: Yes  
*Type*: [S3KeyFilter](aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)