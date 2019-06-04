# AWS::ElasticBeanstalk::ApplicationVersion SourceBundle<a name="aws-properties-beanstalk-sourcebundle"></a>

The `SourceBundle` property is an embedded property of the [AWS::ElasticBeanstalk::ApplicationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-sourcebundle.html) resource\. It specifies the Amazon S3 location of the source bundle for an AWS Elastic Beanstalk application version\.

## Syntax<a name="aws-properties-beanstalk-sourcebundle-syntax"></a>

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

## Properties<a name="aws-properties-beanstalk-sourcebundle-properties"></a>

`S3Bucket`  <a name="cfn-beanstalk-sourcebundle-s3bucket"></a>
The Amazon S3 bucket where the data is located\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Key`  <a name="cfn-beanstalk-sourcebundle-s3key"></a>
The Amazon S3 key where the data is located\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)