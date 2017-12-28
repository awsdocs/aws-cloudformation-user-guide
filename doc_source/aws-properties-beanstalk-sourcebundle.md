# Elastic Beanstalk SourceBundle Property Type<a name="aws-properties-beanstalk-sourcebundle"></a>

The `SourceBundle` property is an embedded property of the [AWS::ElasticBeanstalk::ApplicationVersion](aws-properties-beanstalk-version.md) resource\.

## Syntax<a name="w3ab2c21c14d771b5"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-beanstalk-sourcebundle-syntax.json"></a>

```
{
   "S3Bucket" : String,
   "S3Key" : String
}
```

### YAML<a name="aws-properties-beanstalk-sourcebundle-syntax.yaml"></a>

```
S3Bucket: String
S3Key: String
```

## Members<a name="w3ab2c21c14d771b7"></a>

`S3Bucket`  
The Amazon S3 bucket where the data is located\.  
*Required: *Yes  
*Type*: String

`S3Key`  
The Amazon S3 key where the data is located\.  
*Required: *Yes  
*Type*: String