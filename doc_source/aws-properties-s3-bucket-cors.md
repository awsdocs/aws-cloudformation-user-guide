# Amazon S3 Bucket CorsConfiguration<a name="aws-properties-s3-bucket-cors"></a>

Describes the cross\-origin access configuration for objects in an [ AWS::S3::Bucket](aws-properties-s3-bucket.md) resource\.

## Syntax<a name="w3ab2c21c14e1694b5"></a>

### JSON<a name="aws-properties-s3-bucket-cors-syntax.json"></a>

```
{
  "[CorsRules](#cfn-s3-bucket-cors-corsrule)" : [ CorsRules, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-cors-syntax.yaml"></a>

```
[CorsRules](#cfn-s3-bucket-cors-corsrule):
  - CorsRules
```

## Properties<a name="w3ab2c21c14e1694b7"></a>

`CorsRules`  <a name="cfn-s3-bucket-cors-corsrule"></a>
A set of origins and methods that you allow\.  
*Required*: Yes  
*Type*: [Amazon S3 Bucket CorsRule](aws-properties-s3-bucket-cors-corsrule.md)