# AWS::S3::Bucket TagFilter<a name="aws-properties-s3-bucket-tagfilter"></a>

Specifies tags to use to identify a subset of objects for an Amazon S3 bucket\.

## Syntax<a name="aws-properties-s3-bucket-tagfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-tagfilter-syntax.json"></a>

```
{
  "[Key](#cfn-s3-bucket-tagfilter-key)" : String,
  "[Value](#cfn-s3-bucket-tagfilter-value)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-tagfilter-syntax.yaml"></a>

```
  [Key](#cfn-s3-bucket-tagfilter-key): String
  [Value](#cfn-s3-bucket-tagfilter-value): String
```

## Properties<a name="aws-properties-s3-bucket-tagfilter-properties"></a>

`Key`  <a name="cfn-s3-bucket-tagfilter-key"></a>
The tag key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-s3-bucket-tagfilter-value"></a>
The tag value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-tagfilter--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

