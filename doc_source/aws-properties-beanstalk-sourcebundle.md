# Elastic Beanstalk SourceBundle Property Type<a name="aws-properties-beanstalk-sourcebundle"></a>

The `SourceBundle` property is an embedded property of the [AWS::ElasticBeanstalk::ApplicationVersion](aws-properties-beanstalk-version.md) resource\.

## Syntax<a name="w3ab2c21c14d958b5"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-beanstalk-sourcebundle-syntax.json"></a>

```
{
   "[S3Bucket](#cfn-beanstalk-sourcebundle-s3bucket)" : String,
   "[S3Key](#cfn-beanstalk-sourcebundle-s3key)" : String
}
```

### YAML<a name="aws-properties-beanstalk-sourcebundle-syntax.yaml"></a>

```
[S3Bucket](#cfn-beanstalk-sourcebundle-s3bucket): String
[S3Key](#cfn-beanstalk-sourcebundle-s3key): String
```

## Members<a name="w3ab2c21c14d958b7"></a>

`S3Bucket`  <a name="cfn-beanstalk-sourcebundle-s3bucket"></a>
The Amazon S3 bucket where the data is located\.  
*Required*: Yes  
*Type*: String

`S3Key`  <a name="cfn-beanstalk-sourcebundle-s3key"></a>
The Amazon S3 key where the data is located\.  
*Required*: Yes  
*Type*: String