# AWS::EMR::InstanceGroupConfig ScalingTrigger<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingtrigger"></a>

`ScalingTrigger` is a subproperty of the `ScalingRule` property type\. `ScalingTrigger` determines the conditions that trigger an automatic scaling activity\.

## Syntax<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingtrigger-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingtrigger-syntax.json"></a>

```
{
  "[CloudWatchAlarmDefinition](#cfn-elasticmapreduce-instancegroupconfig-scalingtrigger-cloudwatchalarmdefinition)" : CloudWatchAlarmDefinition
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingtrigger-syntax.yaml"></a>

```
  [CloudWatchAlarmDefinition](#cfn-elasticmapreduce-instancegroupconfig-scalingtrigger-cloudwatchalarmdefinition): 
    CloudWatchAlarmDefinition
```

## Properties<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingtrigger-properties"></a>

`CloudWatchAlarmDefinition`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingtrigger-cloudwatchalarmdefinition"></a>
The definition of a CloudWatch metric alarm\. When the defined alarm conditions are met along with other trigger parameters, scaling activity begins\.  
*Required*: Yes  
*Type*: [CloudWatchAlarmDefinition](aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)