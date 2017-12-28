# Amazon S3 Bucket CorsConfiguration<a name="aws-properties-s3-bucket-cors"></a>

Describes the cross\-origin access configuration for objects in an  AWS::S3::Bucket resource\.

## Syntax<a name="w3ab2c21c14e1479b5"></a>

### JSON<a name="aws-properties-s3-bucket-cors-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule)" : [ CorsRules, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-cors-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule):
  - CorsRules
```

## Properties<a name="w3ab2c21c14e1479b7"></a>

`CorsRules`  
A set of origins and methods that you allow\.  
*Required: *Yes  
*Type*: [Amazon S3 Bucket CorsRule](aws-properties-s3-bucket-cors-corsrule.md)