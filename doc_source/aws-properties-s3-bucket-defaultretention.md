# AWS::S3::Bucket DefaultRetention<a name="aws-properties-s3-bucket-defaultretention"></a>

The default retention period that you want to apply to new objects placed in the specified bucket\.

## Syntax<a name="aws-properties-s3-bucket-defaultretention-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-defaultretention-syntax.json"></a>

```
{
  "[Days](#cfn-s3-bucket-defaultretention-days)" : Integer,
  "[Mode](#cfn-s3-bucket-defaultretention-mode)" : String,
  "[Years](#cfn-s3-bucket-defaultretention-years)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-defaultretention-syntax.yaml"></a>

```
  [Days](#cfn-s3-bucket-defaultretention-days): Integer
  [Mode](#cfn-s3-bucket-defaultretention-mode): String
  [Years](#cfn-s3-bucket-defaultretention-years): Integer
```

## Properties<a name="aws-properties-s3-bucket-defaultretention-properties"></a>

`Days`  <a name="cfn-s3-bucket-defaultretention-days"></a>
The number of days that you want to specify for the default retention period\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-s3-bucket-defaultretention-mode"></a>
The default Object Lock retention mode you want to apply to new objects placed in the specified bucket\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COMPLIANCE | GOVERNANCE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Years`  <a name="cfn-s3-bucket-defaultretention-years"></a>
The number of years that you want to specify for the default retention period\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)