# AWS::S3::Bucket Rule<a name="aws-properties-s3-bucket-lifecycleconfig-rule"></a>

Specifies lifecycle rules for an Amazon S3 bucket\. For more information, see [Put Bucket Lifecycle Configuration](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTlifecycle.html) in the *Amazon S3 API Reference*\.

You must specify at least one of the following properties: `AbortIncompleteMultipartUpload`, `ExpirationDate`, `ExpirationInDays`, `NoncurrentVersionExpirationInDays`, `NoncurrentVersionTransition`, `NoncurrentVersionTransitions`, `Transition`, or `Transitions`\.

## Syntax<a name="aws-properties-s3-bucket-lifecycleconfig-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-lifecycleconfig-rule-syntax.json"></a>

```
{
  "[AbortIncompleteMultipartUpload](#cfn-s3-bucket-rule-abortincompletemultipartupload)" : AbortIncompleteMultipartUpload,
  "[ExpirationDate](#cfn-s3-bucket-lifecycleconfig-rule-expirationdate)" : Timestamp,
  "[ExpirationInDays](#cfn-s3-bucket-lifecycleconfig-rule-expirationindays)" : Integer,
  "[ExpiredObjectDeleteMarker](#cfn-s3-bucket-rule-expiredobjectdeletemarker)" : Boolean,
  "[Id](#cfn-s3-bucket-lifecycleconfig-rule-id)" : String,
  "[NoncurrentVersionExpiration](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration)" : NoncurrentVersionExpiration,
  "[NoncurrentVersionExpirationInDays](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpirationindays)" : Integer,
  "[NoncurrentVersionTransition](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition)" : NoncurrentVersionTransition,
  "[NoncurrentVersionTransitions](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransitions)" : [ NoncurrentVersionTransition, ... ],
  "[ObjectSizeGreaterThan](#cfn-s3-bucket-lifecycleconfig-rule-objectsizegreaterthan)" : Long,
  "[ObjectSizeLessThan](#cfn-s3-bucket-lifecycleconfig-rule-objectsizelessthan)" : Long,
  "[Prefix](#cfn-s3-bucket-lifecycleconfig-rule-prefix)" : String,
  "[Status](#cfn-s3-bucket-lifecycleconfig-rule-status)" : String,
  "[TagFilters](#cfn-s3-bucket-rule-tagfilters)" : [ TagFilter, ... ],
  "[Transition](#cfn-s3-bucket-lifecycleconfig-rule-transition)" : Transition,
  "[Transitions](#cfn-s3-bucket-lifecycleconfig-rule-transitions)" : [ Transition, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-lifecycleconfig-rule-syntax.yaml"></a>

```
  [AbortIncompleteMultipartUpload](#cfn-s3-bucket-rule-abortincompletemultipartupload): 
    AbortIncompleteMultipartUpload
  [ExpirationDate](#cfn-s3-bucket-lifecycleconfig-rule-expirationdate): Timestamp
  [ExpirationInDays](#cfn-s3-bucket-lifecycleconfig-rule-expirationindays): Integer
  [ExpiredObjectDeleteMarker](#cfn-s3-bucket-rule-expiredobjectdeletemarker): Boolean
  [Id](#cfn-s3-bucket-lifecycleconfig-rule-id): String
  [NoncurrentVersionExpiration](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration): 
    NoncurrentVersionExpiration
  [NoncurrentVersionExpirationInDays](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpirationindays): Integer
  [NoncurrentVersionTransition](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition): 
    NoncurrentVersionTransition
  [NoncurrentVersionTransitions](#cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransitions): 
    - NoncurrentVersionTransition
  [ObjectSizeGreaterThan](#cfn-s3-bucket-lifecycleconfig-rule-objectsizegreaterthan): Long
  [ObjectSizeLessThan](#cfn-s3-bucket-lifecycleconfig-rule-objectsizelessthan): Long
  [Prefix](#cfn-s3-bucket-lifecycleconfig-rule-prefix): String
  [Status](#cfn-s3-bucket-lifecycleconfig-rule-status): String
  [TagFilters](#cfn-s3-bucket-rule-tagfilters): 
    - TagFilter
  [Transition](#cfn-s3-bucket-lifecycleconfig-rule-transition): 
    Transition
  [Transitions](#cfn-s3-bucket-lifecycleconfig-rule-transitions): 
    - Transition
```

## Properties<a name="aws-properties-s3-bucket-lifecycleconfig-rule-properties"></a>

`AbortIncompleteMultipartUpload`  <a name="cfn-s3-bucket-rule-abortincompletemultipartupload"></a>
Specifies a lifecycle rule that stops incomplete multipart uploads to an Amazon S3 bucket\.  
*Required*: Conditional  
*Type*: [AbortIncompleteMultipartUpload](aws-properties-s3-bucket-abortincompletemultipartupload.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpirationDate`  <a name="cfn-s3-bucket-lifecycleconfig-rule-expirationdate"></a>
Indicates when objects are deleted from Amazon S3 and Amazon S3 Glacier\. The date value must be in ISO 8601 format\. The time is always midnight UTC\. If you specify an expiration and transition time, you must use the same time unit for both properties \(either in days or by date\)\. The expiration time must also be later than the transition time\.  
*Required*: Conditional  
*Type*: Timestamp  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpirationInDays`  <a name="cfn-s3-bucket-lifecycleconfig-rule-expirationindays"></a>
Indicates the number of days after creation when objects are deleted from Amazon S3 and Amazon S3 Glacier\. If you specify an expiration and transition time, you must use the same time unit for both properties \(either in days or by date\)\. The expiration time must also be later than the transition time\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpiredObjectDeleteMarker`  <a name="cfn-s3-bucket-rule-expiredobjectdeletemarker"></a>
Indicates whether Amazon S3 will remove a delete marker without any noncurrent versions\. If set to true, the delete marker will be removed if there are no noncurrent versions\. This cannot be specified with `ExpirationInDays`, `ExpirationDate`, or `TagFilters`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-s3-bucket-lifecycleconfig-rule-id"></a>
Unique identifier for the rule\. The value can't be longer than 255 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoncurrentVersionExpiration`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration"></a>
Specifies when noncurrent object versions expire\. Upon expiration, Amazon S3 permanently deletes the noncurrent object versions\. You set this lifecycle configuration action on a bucket that has versioning enabled \(or suspended\) to request that Amazon S3 delete noncurrent object versions at a specific period in the object's lifetime\.  
*Required*: No  
*Type*: [NoncurrentVersionExpiration](aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversionexpiration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoncurrentVersionExpirationInDays`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversionexpirationindays"></a>
\(Deprecated\.\) For buckets with versioning enabled \(or suspended\), specifies the time, in days, between when a new version of the object is uploaded to the bucket and when old versions of the object expire\. When object versions expire, Amazon S3 permanently deletes them\. If you specify a transition and expiration time, the expiration time must be later than the transition time\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoncurrentVersionTransition`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition"></a>
\(Deprecated\.\) For buckets with versioning enabled \(or suspended\), specifies when non\-current objects transition to a specified storage class\. If you specify a transition and expiration time, the expiration time must be later than the transition time\. If you specify this property, don't specify the `NoncurrentVersionTransitions` property\.  
*Required*: Conditional  
*Type*: [NoncurrentVersionTransition](aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoncurrentVersionTransitions`  <a name="cfn-s3-bucket-lifecycleconfig-rule-noncurrentversiontransitions"></a>
For buckets with versioning enabled \(or suspended\), one or more transition rules that specify when non\-current objects transition to a specified storage class\. If you specify a transition and expiration time, the expiration time must be later than the transition time\. If you specify this property, don't specify the `NoncurrentVersionTransition` property\.  
*Required*: Conditional  
*Type*: List of [NoncurrentVersionTransition](aws-properties-s3-bucket-lifecycleconfig-rule-noncurrentversiontransition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectSizeGreaterThan`  <a name="cfn-s3-bucket-lifecycleconfig-rule-objectsizegreaterthan"></a>
Specifies the minimum object size in bytes for this rule to apply to\. Objects must be larger than this value in bytes\. For more information about size based rules, see [Lifecycle configuration using size\-based rules](https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-configuration-examples.html#lc-size-rules) in the *Amazon S3 User Guide*\.  
*Required*: No  
*Type*: Long  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectSizeLessThan`  <a name="cfn-s3-bucket-lifecycleconfig-rule-objectsizelessthan"></a>
Specifies the maximum object size in bytes for this rule to apply to\. Objects must be smaller than this value in bytes\. For more information about sized based rules, see [Lifecycle configuration using size\-based rules](https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-configuration-examples.html#lc-size-rules) in the *Amazon S3 User Guide*\.  
*Required*: No  
*Type*: Long  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-lifecycleconfig-rule-prefix"></a>
Object key prefix that identifies one or more objects to which this rule applies\.  
Replacement must be made for object keys containing special characters \(such as carriage returns\) when using XML requests\. For more information, see [ XML related object key constraints](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-keys.html#object-key-xml-related-constraints)\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-s3-bucket-lifecycleconfig-rule-status"></a>
If `Enabled`, the rule is currently being applied\. If `Disabled`, the rule is not currently being applied\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagFilters`  <a name="cfn-s3-bucket-rule-tagfilters"></a>
Tags to use to identify a subset of objects to which the lifecycle rule applies\.  
*Required*: No  
*Type*: List of [TagFilter](aws-properties-s3-bucket-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Transition`  <a name="cfn-s3-bucket-lifecycleconfig-rule-transition"></a>
\(Deprecated\.\) Specifies when an object transitions to a specified storage class\. If you specify an expiration and transition time, you must use the same time unit for both properties \(either in days or by date\)\. The expiration time must also be later than the transition time\. If you specify this property, don't specify the `Transitions` property\.  
*Required*: Conditional  
*Type*: [Transition](aws-properties-s3-bucket-lifecycleconfig-rule-transition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Transitions`  <a name="cfn-s3-bucket-lifecycleconfig-rule-transitions"></a>
One or more transition rules that specify when an object transitions to a specified storage class\. If you specify an expiration and transition time, you must use the same time unit for both properties \(either in days or by date\)\. The expiration time must also be later than the transition time\. If you specify this property, don't specify the `Transition` property\.  
*Required*: Conditional  
*Type*: List of [Transition](aws-properties-s3-bucket-lifecycleconfig-rule-transition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-lifecycleconfig-rule--examples"></a>



### Manage the lifecycle for S3 objects<a name="aws-properties-s3-bucket-lifecycleconfig-rule--examples--Manage_the_lifecycle_for_S3_objects"></a>

The following example template shows an S3 bucket with a lifecycle configuration rule\. The rule applies to all objects with the `glacier` key prefix\. The objects are transitioned to Glacier after one day, and deleted after one year\.

#### JSON<a name="aws-properties-s3-bucket-lifecycleconfig-rule--examples--Manage_the_lifecycle_for_S3_objects--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "Private",
                "LifecycleConfiguration": {
                    "Rules": [
                        {
                            "Id": "GlacierRule",
                            "Prefix": "glacier",
                            "Status": "Enabled",
                            "ExpirationInDays": 365,
                            "Transitions": [
                                {
                                    "TransitionInDays": 1,
                                    "StorageClass": "GLACIER"
                                }
                            ]
                        }
                    ]
                }
            }
        }
    },
    "Outputs": {
        "BucketName": {
            "Value": {
                "Ref": "S3Bucket"
            },
            "Description": "Name of the sample Amazon S3 bucket with a lifecycle configuration."
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-lifecycleconfig-rule--examples--Manage_the_lifecycle_for_S3_objects--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: Private
      LifecycleConfiguration:
        Rules:
          - Id: GlacierRule
            Prefix: glacier
            Status: Enabled
            ExpirationInDays: 365
            Transitions:
              - TransitionInDays: 1
                StorageClass: GLACIER
Outputs:
  BucketName:
    Value: !Ref S3Bucket
    Description: Name of the sample Amazon S3 bucket with a lifecycle configuration.
```

## See also<a name="aws-properties-s3-bucket-lifecycleconfig-rule--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

