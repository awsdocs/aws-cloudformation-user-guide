# AWS::EMR::InstanceGroupConfig MetricDimension<a name="aws-properties-elasticmapreduce-instancegroupconfig-metricdimension"></a>

`MetricDimension` is a subproperty of the `CloudWatchAlarmDefinition` property type\. `MetricDimension` specifies a CloudWatch dimension, which is specified with a `Key` `Value` pair\. The key is known as a `Name` in CloudWatch\. By default, Amazon EMR uses one dimension whose `Key` is `JobFlowID` and `Value` is a variable representing the cluster ID, which is `${emr.clusterId}`\. This enables the automatic scaling rule for EMR to bootstrap when the cluster ID becomes available during cluster creation\.

## Syntax<a name="aws-properties-elasticmapreduce-instancegroupconfig-metricdimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-metricdimension-syntax.json"></a>

```
{
  "[Key](#cfn-elasticmapreduce-instancegroupconfig-metricdimension-key)" : String,
  "[Value](#cfn-elasticmapreduce-instancegroupconfig-metricdimension-value)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-metricdimension-syntax.yaml"></a>

```
  [Key](#cfn-elasticmapreduce-instancegroupconfig-metricdimension-key): String
  [Value](#cfn-elasticmapreduce-instancegroupconfig-metricdimension-value): String
```

## Properties<a name="aws-properties-elasticmapreduce-instancegroupconfig-metricdimension-properties"></a>

`Key`  <a name="cfn-elasticmapreduce-instancegroupconfig-metricdimension-key"></a>
The dimension name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-elasticmapreduce-instancegroupconfig-metricdimension-value"></a>
The dimension value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)