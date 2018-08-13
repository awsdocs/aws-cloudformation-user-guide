# Amazon S3 Bucket S3KeyFilter<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key"></a>

`S3Key` is a property of the [Amazon S3 Bucket NotificationFilter](aws-properties-s3-bucket-notificationconfiguration-config-filter.md) property that specifies the key names of Amazon Simple Storage Service \(Amazon S3\) objects for which to send notifications\.

## Syntax<a name="w3ab2c21c14e1766b5"></a>

### JSON<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-syntax.json"></a>

```
{
  "[Rules](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-syntax.yaml"></a>

```
[Rules](#cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules):
  - Rule
```

## Properties<a name="w3ab2c21c14e1766b7"></a>

`Rules`  <a name="cfn-s3-bucket-notificationconfiguraiton-config-filter-s3key-rules"></a>
The object key name to filter on and whether to filter on the suffix or prefix of the key name\.  
*Required*: Yes  
*Type*: List of [Amazon S3 Bucket FilterRule](aws-properties-s3-bucket-notificationconfiguration-config-filter-s3key-rules.md)