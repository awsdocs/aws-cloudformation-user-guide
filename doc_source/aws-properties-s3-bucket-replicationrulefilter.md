# AWS::S3::Bucket ReplicationRuleFilter<a name="aws-properties-s3-bucket-replicationrulefilter"></a>

A filter that identifies the subset of objects to which the replication rule applies\. A `Filter` must specify exactly one `Prefix`, `TagFilter`, or an `And` child element\.

## Syntax<a name="aws-properties-s3-bucket-replicationrulefilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-replicationrulefilter-syntax.json"></a>

```
{
  "[And](#cfn-s3-bucket-replicationrulefilter-and)" : ReplicationRuleAndOperator,
  "[Prefix](#cfn-s3-bucket-replicationrulefilter-prefix)" : String,
  "[TagFilter](#cfn-s3-bucket-replicationrulefilter-tagfilter)" : TagFilter
}
```

### YAML<a name="aws-properties-s3-bucket-replicationrulefilter-syntax.yaml"></a>

```
  [And](#cfn-s3-bucket-replicationrulefilter-and): 
    ReplicationRuleAndOperator
  [Prefix](#cfn-s3-bucket-replicationrulefilter-prefix): String
  [TagFilter](#cfn-s3-bucket-replicationrulefilter-tagfilter): 
    TagFilter
```

## Properties<a name="aws-properties-s3-bucket-replicationrulefilter-properties"></a>

`And`  <a name="cfn-s3-bucket-replicationrulefilter-and"></a>
A container for specifying rule filters\. The filters determine the subset of objects to which the rule applies\. This element is required only if you specify more than one filter\. For example:   
+ If you specify both a `Prefix` and a `TagFilter`, wrap these filters in an `And` tag\.
+ If you specify a filter based on multiple tags, wrap the `TagFilter` elements in an `And` tag\.
*Required*: No  
*Type*: [ReplicationRuleAndOperator](aws-properties-s3-bucket-replicationruleandoperator.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-replicationrulefilter-prefix"></a>
An object key name prefix that identifies the subset of objects to which the rule applies\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagFilter`  <a name="cfn-s3-bucket-replicationrulefilter-tagfilter"></a>
A container for specifying a tag key and value\.   
The rule applies only to objects that have the tag in their tag set\.  
*Required*: No  
*Type*: [TagFilter](aws-properties-s3-bucket-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)