# AWS::S3::Bucket ObjectLockConfiguration<a name="aws-properties-s3-bucket-objectlockconfiguration"></a>

Places an Object Lock configuration on the specified bucket\. The rule specified in the Object Lock configuration will be applied by default to every new object placed in the specified bucket\. For more information, see [Locking Objects](https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock.html)\. 

## Syntax<a name="aws-properties-s3-bucket-objectlockconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-objectlockconfiguration-syntax.json"></a>

```
{
  "[ObjectLockEnabled](#cfn-s3-bucket-objectlockconfiguration-objectlockenabled)" : String,
  "[Rule](#cfn-s3-bucket-objectlockconfiguration-rule)" : ObjectLockRule
}
```

### YAML<a name="aws-properties-s3-bucket-objectlockconfiguration-syntax.yaml"></a>

```
  [ObjectLockEnabled](#cfn-s3-bucket-objectlockconfiguration-objectlockenabled): String
  [Rule](#cfn-s3-bucket-objectlockconfiguration-rule): 
    ObjectLockRule
```

## Properties<a name="aws-properties-s3-bucket-objectlockconfiguration-properties"></a>

`ObjectLockEnabled`  <a name="cfn-s3-bucket-objectlockconfiguration-objectlockenabled"></a>
Indicates whether this bucket has an Object Lock configuration enabled\. Enable `ObjectLockEnabled` when you apply `ObjectLockConfiguration` to a bucket\.   
*Required*: No  
*Type*: String  
*Allowed values*: `Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rule`  <a name="cfn-s3-bucket-objectlockconfiguration-rule"></a>
Specifies the Object Lock rule for the specified object\. Enable this rule when you apply `ObjectLockConfiguration` to a bucket\. If Object Lock is turned on, bucket settings require both `Mode` and a period of either `Days` or `Years`\. You cannot specify `Days` and `Years` at the same time\. For more information, see [ObjectLockRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket-objectlockrule.html) and [DefaultRetention](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket-defaultretention.html)\.  
*Required*: Conditional  
*Type*: [ObjectLockRule](aws-properties-s3-bucket-objectlockrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-objectlockconfiguration--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

