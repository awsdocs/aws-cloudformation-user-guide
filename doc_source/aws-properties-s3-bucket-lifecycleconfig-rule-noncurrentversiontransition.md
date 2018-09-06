# Amazon S3 Bucket NoncurrentVersionTransition<a name="aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition"></a>

`NoncurrentVersionTransition` is a property of the [Amazon S3 Bucket Rule](aws-properties-s3-bucket-lifecycleconfig-rule.md) property that describes when noncurrent objects transition to a specified storage class\.

## Syntax<a name="w3ab2c21c14e1736b5"></a>

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

## Properties<a name="w3ab2c21c14e1736b7"></a>

`StorageClass`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-storageclass"></a>
The storage class to which you want the object to transition, such as `GLACIER`\. For valid values, see the `StorageClass` request element of the [PUT Bucket lifecycle](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTlifecycle.html) action in the *Amazon Simple Storage Service API Reference*\.  
*Required*: Yes  
*Type*: String

`TransitionInDays`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition-transitionindays"></a>
The number of days between the time that a new version of the object is uploaded to the bucket and when old versions of the object are transitioned to the specified storage class\.  
*Required*: Yes  
*Type*: Integer