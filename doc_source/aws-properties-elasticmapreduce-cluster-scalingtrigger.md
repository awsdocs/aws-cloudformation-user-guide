# Amazon EMR Cluster ScalingTrigger<a name="aws-properties-elasticmapreduce-cluster-scalingtrigger"></a>

The `ScalingTrigger` property type specifies the conditions that trigger an automatic scaling activity\. `ScalingTrigger` is the property type for the `Trigger` subproperty of the [Amazon EMR Cluster ScalingRule](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule.md) property type\.

## Syntax<a name="w3ab2c21c14d936b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-cluster-scalingtrigger-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition)" : CloudWatchAlarmDefinition
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-scalingtrigger-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition): CloudWatchAlarmDefinition
```

## Properties<a name="w3ab2c21c14d936b7"></a>

`CloudWatchAlarmDefinition`  
The definition of a CloudWatch metric alarm\. When the defined alarm conditions are met along with other trigger parameters, scaling activity begins\.  
*Required: *Yes  
*Type*: [Amazon EMR Cluster CloudWatchAlarmDefinition](aws-properties-elasticmapreduce-cluster-cloudwatchalarmdefinition.md)  
*Update requires*: No interruption