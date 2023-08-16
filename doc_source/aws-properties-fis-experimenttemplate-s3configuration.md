# AWS::FIS::ExperimentTemplate S3Configuration<a name="aws-properties-fis-experimenttemplate-s3configuration"></a>

Specifies the configuration for experiment logging to Amazon S3\.

## Syntax<a name="aws-properties-fis-experimenttemplate-s3configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-s3configuration-syntax.json"></a>

```
{
  "[BucketName](#cfn-fis-experimenttemplate-s3configuration-bucketname)" : String,
  "[Prefix](#cfn-fis-experimenttemplate-s3configuration-prefix)" : String
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-s3configuration-syntax.yaml"></a>

```
  [BucketName](#cfn-fis-experimenttemplate-s3configuration-bucketname): String
  [Prefix](#cfn-fis-experimenttemplate-s3configuration-prefix): String
```

## Properties<a name="aws-properties-fis-experimenttemplate-s3configuration-properties"></a>

`BucketName`  <a name="cfn-fis-experimenttemplate-s3configuration-bucketname"></a>
The name of the destination bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-fis-experimenttemplate-s3configuration-prefix"></a>
The bucket prefix\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `[\s\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)