# Amazon EMR InstanceGroupConfig ScalingRule<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingrule"></a>

The `ScalingRule` property type represents a scale\-in or scale\-out rule that defines scaling activity, including the CloudWatch metric alarm that triggers activity, how EC2 instances are added or removed, and the periodicity of adjustments\. The `Rules` subproperty of the [Amazon EMR InstanceGroupConfig AutoScalingPolicy](aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy.md) property contains a list of one or more `ScalingRule` property types\.

## Syntax<a name="w3ab2c21c14e1192b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingrule-syntax.json"></a>

```
{
  "[Action](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-action)" : ScalingAction,
  "[Description](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-description)" : String,
  "[Name](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-name)" : String,
  "[Trigger](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-trigger)" : ScalingTrigger
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingrule-syntax.yaml"></a>

```
  [Action](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-action): ScalingAction
  [Description](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-description): String
  [Name](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-name): String
  [Trigger](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-trigger): ScalingTrigger
```

## Properties<a name="w3ab2c21c14e1192b7"></a>

`Action`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingrule-action"></a>
The conditions that trigger an automatic scaling activity\.  
*Required*: Yes  
*Type*: [Amazon EMR InstanceGroupConfig ScalingAction](aws-properties-elasticmapreduce-instancegroupconfig-scalingaction.md)

`Description`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingrule-description"></a>
A friendly, more verbose description of the automatic scaling rule\.  
*Required*: No  
*Type*: String

`Name`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingrule-name"></a>
The identifier of the automatic scaling rule\. Rule names must be unique within a scaling policy\.  
*Required*: Yes  
*Type*: String

`Trigger`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingrule-trigger"></a>
The CloudWatch alarm definition that determines when automatic scaling activity is triggered\.  
*Required*: Yes  
*Type*: [Amazon EMR InstanceGroupConfig ScalingTrigger](aws-properties-elasticmapreduce-instancegroupconfig-scalingtrigger.md)