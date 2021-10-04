# AWS::S3Outposts::Bucket LifecycleConfiguration<a name="aws-properties-s3outposts-bucket-lifecycleconfiguration"></a>

The container for the lifecycle configuration for the objects stored in an S3 on Outposts bucket\.

## Syntax<a name="aws-properties-s3outposts-bucket-lifecycleconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3outposts-bucket-lifecycleconfiguration-syntax.json"></a>

```
{
  "[Rules](#cfn-s3outposts-bucket-lifecycleconfiguration-rules)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-s3outposts-bucket-lifecycleconfiguration-syntax.yaml"></a>

```
  [Rules](#cfn-s3outposts-bucket-lifecycleconfiguration-rules): 
    - Rule
```

## Properties<a name="aws-properties-s3outposts-bucket-lifecycleconfiguration-properties"></a>

`Rules`  <a name="cfn-s3outposts-bucket-lifecycleconfiguration-rules"></a>
The container for the lifecycle configuration rules for the objects stored in the S3 on Outposts bucket\.  
*Required*: Yes  
*Type*: List of [Rule](aws-properties-s3outposts-bucket-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)