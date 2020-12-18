# AWS::S3::Bucket Transition<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition"></a>

Specifies when an object transitions to a specified storage class\. For more information about Amazon S3 lifecycle configuration rules, see [Transitioning Objects Using Amazon S3 Lifecycle](https://docs.aws.amazon.com/AmazonS3/latest/dev/lifecycle-transition-general-considerations.html) in the *Amazon Simple Storage Service Developer Guide*\.

## Syntax<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition-syntax.json"></a>

```
{
  "[StorageClass](#cfn-s3-bucket-lifecycleconfig-rule-transition-storageclass)" : String,
  "[TransitionDate](#cfn-s3-bucket-lifecycleconfig-rule-transition-transitiondate)" : Timestamp,
  "[TransitionInDays](#cfn-s3-bucket-lifecycleconfig-rule-transition-transitionindays)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition-syntax.yaml"></a>

```
  [StorageClass](#cfn-s3-bucket-lifecycleconfig-rule-transition-storageclass): String
  [TransitionDate](#cfn-s3-bucket-lifecycleconfig-rule-transition-transitiondate): Timestamp
  [TransitionInDays](#cfn-s3-bucket-lifecycleconfig-rule-transition-transitionindays): Integer
```

## Properties<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition-properties"></a>

`StorageClass`  <a name="cfn-s3-bucket-lifecycleconfig-rule-transition-storageclass"></a>
The storage class to which you want the object to transition\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DEEP_ARCHIVE | GLACIER | INTELLIGENT_TIERING | ONEZONE_IA | STANDARD_IA`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitionDate`  <a name="cfn-s3-bucket-lifecycleconfig-rule-transition-transitiondate"></a>
Indicates when objects are transitioned to the specified storage class\. The date value must be in ISO 8601 format\. The time is always midnight UTC\.  
*Required*: Conditional  
*Type*: Timestamp  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitionInDays`  <a name="cfn-s3-bucket-lifecycleconfig-rule-transition-transitionindays"></a>
Indicates the number of days after creation when objects are transitioned to the specified storage class\. The value must be a positive integer\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

