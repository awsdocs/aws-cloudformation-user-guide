# Amazon EMR Cluster ScalingTrigger<a name="aws-properties-elasticmapreduce-cluster-scalingtrigger"></a>

The `ScalingTrigger` property type specifies the conditions that trigger an automatic scaling activity\. `ScalingTrigger` is the property type for the `Trigger` subproperty of the [Amazon EMR Cluster ScalingRule](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule.md) property type\.

## Syntax<a name="w3ab2c21c14e1127b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-cluster-scalingtrigger-syntax.json"></a>

```
{
  "[CloudWatchAlarmDefinition](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition)" : CloudWatchAlarmDefinition
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-scalingtrigger-syntax.yaml"></a>

```
  [CloudWatchAlarmDefinition](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition): CloudWatchAlarmDefinition
```

## Properties<a name="w3ab2c21c14e1127b7"></a>

`CloudWatchAlarmDefinition`  <a name="cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition"></a>
The definition of a CloudWatch metric alarm\. When the defined alarm conditions are met along with other trigger parameters, scaling activity begins\.  
*Required*: Yes  
*Type*: [Amazon EMR Cluster CloudWatchAlarmDefinition](aws-properties-elasticmapreduce-cluster-cloudwatchalarmdefinition.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)