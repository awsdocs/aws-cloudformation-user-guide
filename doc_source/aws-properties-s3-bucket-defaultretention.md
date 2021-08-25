# AWS::S3::Bucket DefaultRetention<a name="aws-properties-s3-bucket-defaultretention"></a>

The container element for specifying the default Object Lock retention settings for new objects placed in the specified bucket\.

**Note**  
The `DefaultRetention` settings require both a mode and a period\.
The `DefaultRetention` period can be either `Days` or `Years` but you must select one\. You cannot specify `Days` and `Years` at the same time\.

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
The number of days that you want to specify for the default retention period\. If Object Lock is turned on, you must specify `Mode` and specify either `Days` or `Years`\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-s3-bucket-defaultretention-mode"></a>
The default Object Lock retention mode you want to apply to new objects placed in the specified bucket\. If Object Lock is turned on, you must specify `Mode` and specify either `Days` or `Years`\.  
*Required*: Conditional  
*Type*: String  
*Allowed values*: `COMPLIANCE | GOVERNANCE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Years`  <a name="cfn-s3-bucket-defaultretention-years"></a>
The number of years that you want to specify for the default retention period\. If Object Lock is turned on, you must specify `Mode` and specify either `Days` or `Years`\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-defaultretention--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

