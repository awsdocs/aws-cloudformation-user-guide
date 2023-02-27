# AWS::Macie::AllowList S3WordsList<a name="aws-properties-macie-allowlist-s3wordslist"></a>

Specifies the location and name of an Amazon Simple Storage Service \(Amazon S3\) object that lists specific, predefined text to ignore when inspecting data sources for sensitive data\.

## Syntax<a name="aws-properties-macie-allowlist-s3wordslist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-macie-allowlist-s3wordslist-syntax.json"></a>

```
{
  "[BucketName](#cfn-macie-allowlist-s3wordslist-bucketname)" : String,
  "[ObjectKey](#cfn-macie-allowlist-s3wordslist-objectkey)" : String
}
```

### YAML<a name="aws-properties-macie-allowlist-s3wordslist-syntax.yaml"></a>

```
  [BucketName](#cfn-macie-allowlist-s3wordslist-bucketname): String
  [ObjectKey](#cfn-macie-allowlist-s3wordslist-objectkey): String
```

## Properties<a name="aws-properties-macie-allowlist-s3wordslist-properties"></a>

`BucketName`  <a name="cfn-macie-allowlist-s3wordslist-bucketname"></a>
The full name of the S3 bucket that contains the object\. This value correlates to the `Name` field of a bucket's properties in Amazon S3\.  
This value is case sensitive\. In addition, don't use wildcard characters or specify partial values for the name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectKey`  <a name="cfn-macie-allowlist-s3wordslist-objectkey"></a>
The full name of the S3 object\. This value correlates to the `Key` field of an object's properties in Amazon S3\. If the name includes a path, include the complete path\. For example, `AllowLists/Macie/MyList.txt`\.  
This value is case sensitive\. In addition, don't use wildcard characters or specify partial values for the name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)