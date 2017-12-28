# Amazon S3 Bucket Rule<a name="aws-properties-s3-bucket-lifecycleconfig-rule"></a>

The `Rule` property type describes lifecycle rules\. The `Rules` subproperty of the [Amazon S3 Bucket LifecycleConfiguration](aws-properties-s3-bucket-lifecycleconfig.md) property contains a list of `Rule` property types\. For more information, see [PUT Bucket lifecycle](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTlifecycle.html) in the *Amazon Simple Storage Service \(Amazon S3\) API Reference*\.

## Syntax<a name="w3ab2c21c14e1528b5"></a>

### JSON<a name="aws-properties-s3-bucket-lifecycleconfig-rule-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-rule-abortincompletemultipartupload)" : AbortIncompleteMultipartUpload,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-expirationdate)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-expirationindays)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-id)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpirationindays)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition)" : NoncurrentVersionTransition,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransitions)" : [ NoncurrentVersionTransition, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-prefix)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-status)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-rule-tagfilters)" : [ TagFilter, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-transition)" : Transition,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-transitions)" : [ Transition, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-lifecycleconfig-rule-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-rule-abortincompletemultipartupload): 
  AbortIncompleteMultipartUpload
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-expirationdate): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-expirationindays): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-id): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpirationindays): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition):
  NoncurrentVersionTransition
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransitions):
  - NoncurrentVersionTransition
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-prefix): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-status): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-rule-tagfilters): 
  - TagFilter
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-transition):
  Transition
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-lifecycleconfig-rule-transitions):
  - Transition
```

## Properties<a name="w3ab2c21c14e1528b7"></a>

`AbortIncompleteMultipartUpload`  
Specifies a lifecycle rule that aborts incomplete multipart uploads to an Amazon S3 bucket\.  
*Required: *Conditional\. You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.  
*Type*: [Amazon S3 Bucket AbortIncompleteMultipartUpload](aws-properties-s3-bucket-abortincompletemultipartupload.md)

`ExpirationDate`  
Indicates when objects are deleted from Amazon S3 and Amazon Glacier\. The date value must be in ISO 8601 format\. The time is always midnight UTC\. If you specify an expiration and transition time, you must use the same time unit for both properties \(either in days or by date\)\. The expiration time must also be later than the transition time\.  
*Required: *Conditional\. You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.  
*Type*: String

`ExpirationInDays`  
Indicates the number of days after creation when objects are deleted from Amazon S3 and Amazon Glacier\. If you specify an expiration and transition time, you must use the same time unit for both properties \(either in days or by date\)\. The expiration time must also be later than the transition time\.  
*Required: *Conditional\. You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.  
*Type*: Integer

`Id`  
A unique identifier for this rule\. The value cannot be more than 255 characters\.  
*Required: *No  
*Type*: String

`NoncurrentVersionExpirationInDays`  
For buckets with versioning enabled \(or suspended\), specifies the time, in days, between when a new version of the object is uploaded to the bucket and when old versions of the object expire\. When object versions expire, Amazon S3 permanently deletes them\. If you specify a transition and expiration time, the expiration time must be later than the transition time\.  
*Required: *Conditional\. You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.  
*Type*: Integer

`NoncurrentVersionTransition` \(deprecated\)  
For buckets with versioning enabled \(or suspended\), specifies when non\-current objects transition to a specified storage class\. If you specify a transition and expiration time, the expiration time must be later than the transition time\. If you specify this property, don't specify the `NoncurrentVersionTransitions` property\.  
*Required: *Conditional\. You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.  
*Type*: [Amazon S3 Bucket NoncurrentVersionTransition](aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition.md)

`NoncurrentVersionTransitions`  
For buckets with versioning enabled \(or suspended\), one or more transition rules that specify when non\-current objects transition to a specified storage class\. If you specify a transition and expiration time, the expiration time must be later than the transition time\. If you specify this property, don't specify the `NoncurrentVersionTransition` property\.  
*Required: *Conditional\. You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.  
*Type*: List of [Amazon S3 Bucket NoncurrentVersionTransition](aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition.md)

`Prefix`  
Object key prefix that identifies one or more objects to which this rule applies\.  
*Required: *No  
*Type*: String

`Status`  
Specify either `Enabled` or `Disabled`\. If you specify `Enabled`, Amazon S3 executes this rule as scheduled\. If you specify `Disabled`, Amazon S3 ignores this rule\.  
*Required: *Yes  
*Type*: String

`TagFilters`  
Tags to use to identify a subset of objects to which the lifecycle rule applies\.  
 *Required*: No  
 *Type*: List of [Amazon S3 Bucket TagFilter](aws-properties-s3-bucket-tagfilter.md)  
 *Update requires*: No interruption 

`Transition` \(deprecated\)  
Specifies when an object transitions to a specified storage class\. If you specify an expiration and transition time, you must use the same time unit for both properties \(either in days or by date\)\. The expiration time must also be later than the transition time\. If you specify this property, don't specify the `Transitions` property\.  
*Required: *Conditional\. You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.  
*Type*: [Amazon S3 Bucket Transition](aws-properties-s3-bucket-lifecycleconfig-rule-transition.md)

`Transitions`  
One or more transition rules that specify when an object transitions to a specified storage class\. If you specify an expiration and transition time, you must use the same time unit for both properties \(either in days or by date\)\. The expiration time must also be later than the transition time\. If you specify this property, don't specify the `Transition` property\.  
*Required: *Conditional\. You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.  
*Type*: List of [Amazon S3 Bucket Transition](aws-properties-s3-bucket-lifecycleconfig-rule-transition.md)