# Amazon S3 Bucket TagFilter<a name="aws-properties-s3-bucket-tagfilter"></a>

<a name="aws-properties-s3-bucket-tagfilter-description"></a>The `TagFilter` property type specifies tags to use to identify a subset of objects for an Amazon S3 bucket\.

<a name="aws-properties-s3-bucket-tagfilter-inheritance"></a> The `TagFilters` property of the [AWS::S3::Bucket](aws-properties-s3-bucket.md) property type contains a list of `TagFilter` property types\. 

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
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-s3-bucket-tagfilter-value"></a>
The tag value\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 