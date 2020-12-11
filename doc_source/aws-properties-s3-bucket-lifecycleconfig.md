# AWS::S3::Bucket LifecycleConfiguration<a name="aws-properties-s3-bucket-lifecycleconfig"></a>

Specifies the lifecycle configuration for objects in an Amazon S3 bucket\. For more information, see [Object Lifecycle Management](https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html) in the *Amazon Simple Storage Service Developer Guide*\.

## Syntax<a name="aws-properties-s3-bucket-lifecycleconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-lifecycleconfig-syntax.json"></a>

```
{
  "[Rules](#cfn-s3-bucket-lifecycleconfig-rules)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-lifecycleconfig-syntax.yaml"></a>

```
  [Rules](#cfn-s3-bucket-lifecycleconfig-rules): 
    - Rule
```

## Properties<a name="aws-properties-s3-bucket-lifecycleconfig-properties"></a>

`Rules`  <a name="cfn-s3-bucket-lifecycleconfig-rules"></a>
A lifecycle rule for individual objects in an Amazon S3 bucket\.  
*Required*: Yes  
*Type*: List of [Rule](aws-properties-s3-bucket-lifecycleconfig-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-lifecycleconfig--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

