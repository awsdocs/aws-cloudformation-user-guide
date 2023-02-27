# AWS::S3Outposts::Bucket Filter<a name="aws-properties-s3outposts-bucket-filter"></a>

<a name="aws-properties-s3outposts-bucket-filter-description"></a>The `Filter` property type specifies Property description not available\. for an [AWS::S3Outposts::Bucket](aws-resource-s3outposts-bucket.md)\.

## Syntax<a name="aws-properties-s3outposts-bucket-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3outposts-bucket-filter-syntax.json"></a>

```
{
  "[AndOperator](#cfn-s3outposts-bucket-filter-andoperator)" : FilterAndOperator,
  "[Prefix](#cfn-s3outposts-bucket-filter-prefix)" : String,
  "[Tag](#cfn-s3outposts-bucket-filter-tag)" : FilterTag
}
```

### YAML<a name="aws-properties-s3outposts-bucket-filter-syntax.yaml"></a>

```
  [AndOperator](#cfn-s3outposts-bucket-filter-andoperator): 
    FilterAndOperator
  [Prefix](#cfn-s3outposts-bucket-filter-prefix): String
  [Tag](#cfn-s3outposts-bucket-filter-tag): 
    FilterTag
```

## Properties<a name="aws-properties-s3outposts-bucket-filter-properties"></a>

`AndOperator`  <a name="cfn-s3outposts-bucket-filter-andoperator"></a>
Property description not available\.  
*Required*: No  
*Type*: [FilterAndOperator](aws-properties-s3outposts-bucket-filterandoperator.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3outposts-bucket-filter-prefix"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tag`  <a name="cfn-s3outposts-bucket-filter-tag"></a>
Property description not available\.  
*Required*: No  
*Type*: [FilterTag](aws-properties-s3outposts-bucket-filtertag.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)