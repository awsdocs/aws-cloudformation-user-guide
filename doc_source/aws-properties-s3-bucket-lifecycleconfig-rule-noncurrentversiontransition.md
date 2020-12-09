# AWS::S3::Bucket NoncurrentVersionTransition<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition"></a>

Container for the transition rule that describes when noncurrent objects transition to the `STANDARD_IA`, `ONEZONE_IA`, `INTELLIGENT_TIERING`, `GLACIER`, or `DEEP_ARCHIVE` storage class\. If your bucket is versioning\-enabled \(or versioning is suspended\), you can set this action to request that Amazon S3 transition noncurrent object versions to the `STANDARD_IA`, `ONEZONE_IA`, `INTELLIGENT_TIERING`, `GLACIER`, or `DEEP_ARCHIVE` storage class at a specific period in the object's lifetime\.

## Syntax<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-syntax.json"></a>

```
{
  "[StorageClass](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-storageclass)" : String,
  "[TransitionInDays](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-transitionindays)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-syntax.yaml"></a>

```
  [StorageClass](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-storageclass): String
  [TransitionInDays](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-transitionindays): Integer
```

## Properties<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-properties"></a>

`StorageClass`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-storageclass"></a>
The class of storage used to store the object\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DEEP_ARCHIVE | GLACIER | INTELLIGENT_TIERING | ONEZONE_IA | STANDARD_IA`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitionInDays`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-transitionindays"></a>
Specifies the number of days an object is noncurrent before Amazon S3 can perform the associated action\. For information about the noncurrent days calculations, see [How Amazon S3 Calculates How Long an Object Has Been Noncurrent](https://docs.aws.amazon.com/AmazonS3/latest/dev/intro-lifecycle-rules.html#non-current-days-calculations) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)