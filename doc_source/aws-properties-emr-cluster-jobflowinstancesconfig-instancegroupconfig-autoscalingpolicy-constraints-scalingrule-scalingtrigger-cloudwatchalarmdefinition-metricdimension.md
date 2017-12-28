# Amazon EMR Cluster MetricDimension<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-scalingtrigger-cloudwatchalarmdefinition-metricdimension"></a>

The `MetricDimension` property type represents a CloudWatch dimension that you specify using a key–value pair\. The `Dimensions` subproperty of the [Amazon EMR Cluster CloudWatchAlarmDefinition](aws-properties-elasticmapreduce-cluster-cloudwatchalarmdefinition.md) property contains a list of one or more `MetricDimension` property types\.

## Syntax<a name="w3ab2c21c14d912b5"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-scalingtrigger-cloudwatchalarmdefinition-metricdimension-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-scalingtrigger-cloudwatchalarmdefinition-metricdimension-cloudwatchalarmdefinition-key)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-scalingtrigger-cloudwatchalarmdefinition-metricdimension-cloudwatchalarmdefinition-value)" : String
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-scalingtrigger-cloudwatchalarmdefinition-metricdimension-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-scalingtrigger-cloudwatchalarmdefinition-metricdimension-cloudwatchalarmdefinition-key): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-scalingtrigger-cloudwatchalarmdefinition-metricdimension-cloudwatchalarmdefinition-value): String
```

## Properties<a name="w3ab2c21c14d912b7"></a>

By default, Amazon EMR uses one dimension whose key \(known as a `Name` in CloudWatch\) is `JobFlowID` and whose value is a variable representing the cluster ID, which is `${emr.clusterId}`\. This enables the rule to bootstrap when the cluster ID becomes available\.

`Key`  
The dimension name\.  
*Required: *Yes  
*Type*: String

`Value`  
The dimension value\.  
*Required: *Yes  
*Type*: String