# AWS::S3::Bucket NoncurrentVersionExpiration<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration"></a>

Specifies when noncurrent object versions expire\. Upon expiration, Amazon S3 permanently deletes the noncurrent object versions\. You set this lifecycle configuration action on a bucket that has versioning enabled \(or suspended\) to request that Amazon S3 delete noncurrent object versions at a specific period in the object's lifetime\.

## Syntax<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-syntax.json"></a>

```
{
  "[NewerNoncurrentVersions](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-newernoncurrentversions)" : Integer,
  "[NoncurrentDays](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-noncurrentdays)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-syntax.yaml"></a>

```
  [NewerNoncurrentVersions](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-newernoncurrentversions): Integer
  [NoncurrentDays](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-noncurrentdays): Integer
```

## Properties<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-properties"></a>

`NewerNoncurrentVersions`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-newernoncurrentversions"></a>
Specifies how many noncurrent versions Amazon S3 will retain\. If there are this many more recent noncurrent versions, Amazon S3 will take the associated action\. For more information about noncurrent versions, see [Lifecycle configuration elements](https://docs.aws.amazon.com/AmazonS3/latest/userguide/intro-lifecycle-rules.html) in the *Amazon S3 User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoncurrentDays`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration-noncurrentdays"></a>
Specifies the number of days an object is noncurrent before Amazon S3 can perform the associated action\. For information about the noncurrent days calculations, see [How Amazon S3 Calculates When an Object Became Noncurrent](https://docs.aws.amazon.com/AmazonS3/latest/dev/intro-lifecycle-rules.html#non-current-days-calculations) in the *Amazon S3 User Guide*\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)