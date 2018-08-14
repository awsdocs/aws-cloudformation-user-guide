# Amazon S3 Bucket Transition<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition"></a>

Describes when an object transitions to a specified storage class for the [Amazon S3 Bucket Rule](aws-properties-s3-bucket-lifecycleconfig-rule.md) property\.

## Syntax<a name="w3ab2c21c14e1796b5"></a>

### JSON<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition-syntax.json"></a>

```
{
  "[StorageClass](#cfn-s3-bucket-lifecycleconfig-rule-transition-storageclass)" : String,
  "[TransitionDate](#cfn-s3-bucket-lifecycleconfig-rule-transition-transitiondate)" : String,
  "[TransitionInDays](#cfn-s3-bucket-lifecycleconfig-rule-transition-transitionindays)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-lifecycleconfig-rule-transition-syntax.yaml"></a>

```
[StorageClass](#cfn-s3-bucket-lifecycleconfig-rule-transition-storageclass): String
[TransitionDate](#cfn-s3-bucket-lifecycleconfig-rule-transition-transitiondate): String
[TransitionInDays](#cfn-s3-bucket-lifecycleconfig-rule-transition-transitionindays): Integer
```

## Properties<a name="w3ab2c21c14e1796b7"></a>

`StorageClass`  <a name="cfn-s3-bucket-lifecycleconfig-rule-transition-storageclass"></a>
The storage class to which you want the object to transition, such as `GLACIER`\. For valid values, see the `StorageClass` request element of the [PUT Bucket lifecycle](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTlifecycle.html) action in the *Amazon Simple Storage Service API Reference*\.  
*Required*: Yes  
*Type*: String

`TransitionDate`  <a name="cfn-s3-bucket-lifecycleconfig-rule-transition-transitiondate"></a>
Indicates when objects are transitioned to the specified storage class\. The date value must be in ISO 8601 format\. The time is always midnight UTC\.  
*Required*: Conditional  
*Type*: String

`TransitionInDays`  <a name="cfn-s3-bucket-lifecycleconfig-rule-transition-transitionindays"></a>
Indicates the number of days after creation when objects are transitioned to the specified storage class\.  
*Required*: Conditional  
*Type*: Integer