# AWS::S3::Bucket ReplicationRuleAndOperator<a name="aws-properties-s3-bucket-replicationruleandoperator"></a>

A container for specifying rule filters\. The filters determine the subset of objects to which the rule applies\. This element is required only if you specify more than one filter\. 

For example:
+ If you specify both a `Prefix` and a `TagFilter`, wrap these filters in an `And` tag\. 
+ If you specify a filter based on multiple tags, wrap the `TagFilter` elements in an `And` tag

## Syntax<a name="aws-properties-s3-bucket-replicationruleandoperator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-replicationruleandoperator-syntax.json"></a>

```
{
  "[Prefix](#cfn-s3-bucket-replicationruleandoperator-prefix)" : String,
  "[TagFilters](#cfn-s3-bucket-replicationruleandoperator-tagfilters)" : [ TagFilter, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-replicationruleandoperator-syntax.yaml"></a>

```
  [Prefix](#cfn-s3-bucket-replicationruleandoperator-prefix): String
  [TagFilters](#cfn-s3-bucket-replicationruleandoperator-tagfilters): 
    - TagFilter
```

## Properties<a name="aws-properties-s3-bucket-replicationruleandoperator-properties"></a>

`Prefix`  <a name="cfn-s3-bucket-replicationruleandoperator-prefix"></a>
An object key name prefix that identifies the subset of objects to which the rule applies\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagFilters`  <a name="cfn-s3-bucket-replicationruleandoperator-tagfilters"></a>
An array of tags containing key and value pairs\.  
*Required*: No  
*Type*: List of [TagFilter](aws-properties-s3-bucket-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)