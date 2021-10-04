# AWS::S3::Bucket ObjectLockRule<a name="aws-properties-s3-bucket-objectlockrule"></a>

Specifies the Object Lock rule for the specified object\. Enable the this rule when you apply `ObjectLockConfiguration` to a bucket\.

## Syntax<a name="aws-properties-s3-bucket-objectlockrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-objectlockrule-syntax.json"></a>

```
{
  "[DefaultRetention](#cfn-s3-bucket-objectlockrule-defaultretention)" : DefaultRetention
}
```

### YAML<a name="aws-properties-s3-bucket-objectlockrule-syntax.yaml"></a>

```
  [DefaultRetention](#cfn-s3-bucket-objectlockrule-defaultretention): 
    DefaultRetention
```

## Properties<a name="aws-properties-s3-bucket-objectlockrule-properties"></a>

`DefaultRetention`  <a name="cfn-s3-bucket-objectlockrule-defaultretention"></a>
The default Object Lock retention mode and period that you want to apply to new objects placed in the specified bucket\. If Object Lock is turned on, bucket settings require both `Mode` and a period of either `Days` or `Years`\. You cannot specify `Days` and `Years` at the same time\. For more information about allowable values for mode and period, see [DefaultRetention](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket-defaultretention.html)\.  
*Required*: Conditional  
*Type*: [DefaultRetention](aws-properties-s3-bucket-defaultretention.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)