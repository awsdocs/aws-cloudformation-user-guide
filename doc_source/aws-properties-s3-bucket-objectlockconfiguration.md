# AWS::S3::Bucket ObjectLockConfiguration<a name="aws-properties-s3-bucket-objectlockconfiguration"></a>

Places an object lock configuration on the specified bucket\. The rule specified in the object lock configuration will be applied by default to every new object placed in the specified bucket\.

## Syntax<a name="aws-properties-s3-bucket-objectlockconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-objectlockconfiguration-syntax.json"></a>

```
{
  "[ObjectLockEnabled](#cfn-s3-bucket-objectlockconfiguration-objectlockenabled)" : String,
  "[Rule](#cfn-s3-bucket-objectlockconfiguration-rule)" : [ObjectLockRule](aws-properties-s3-bucket-objectlockrule.md)
}
```

### YAML<a name="aws-properties-s3-bucket-objectlockconfiguration-syntax.yaml"></a>

```
  [ObjectLockEnabled](#cfn-s3-bucket-objectlockconfiguration-objectlockenabled): String
  [Rule](#cfn-s3-bucket-objectlockconfiguration-rule):
    [ObjectLockRule](aws-properties-s3-bucket-objectlockrule.md)
```

## Properties<a name="aws-properties-s3-bucket-objectlockconfiguration-properties"></a>

`ObjectLockEnabled`  <a name="cfn-s3-bucket-objectlockconfiguration-objectlockenabled"></a>
Indicates whether this bucket has an object lock configuration enabled\.
*Required*: No
*Type*: String
*Allowed Values*: `Enabled`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rule`  <a name="cfn-s3-bucket-objectlockconfiguration-rule"></a>
The object lock rule in place for the specified object\.
*Required*: No
*Type*: [ObjectLockRule](aws-properties-s3-bucket-objectlockrule.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
