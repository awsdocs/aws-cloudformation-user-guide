# AWS::S3::Bucket ObjectLockRule<a name="aws-properties-s3-bucket-objectlockrule"></a>

The Object Lock rule in place for the specified object\.

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
The default retention period that you want to apply to new objects placed in the specified bucket\. Bucket default settings require both a mode and a period\.  
*Required*: No  
*Type*: [DefaultRetention](aws-properties-s3-bucket-defaultretention.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)