# Amazon EMR Cluster ScalingRule<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule"></a>

The `ScalingRule` property type represents a scale\-in or scale\-out rule that defines scaling activity, including the CloudWatch metric alarm that triggers activity, how Amazon EC2 instances are added or removed, and the periodicity of adjustments\. The `Rules` subproperty of the [Amazon EMR Cluster JobFlowInstancesConfig](aws-properties-emr-cluster-jobflowinstancesconfig.md) property contains a list of one or more `ScalingRule` property types\.

## Syntax<a name="w3ab2c21c14e1121b5"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-syntax.json"></a>

```
{
  "[Action](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-action)" : ScalingAction,
  "[Description](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-description)" : String,
  "[Name](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-name)" : String,
  "[Trigger](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-trigger)" : ScalingTrigger
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-syntax.yaml"></a>

```
  [Action](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-action): ScalingAction
  [Description](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-description): String
  [Name](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-name): String
  [Trigger](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-trigger): ScalingTrigger
```

## Properties<a name="w3ab2c21c14e1121b7"></a>

`Action`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-action"></a>
The conditions that trigger an automatic scaling activity\.  
*Required*: Yes  
*Type:* [Amazon EMR Cluster ScalingAction](aws-properties-elasticmapreduce-cluster-scalingaction.md)

`Description`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-description"></a>
A friendly, more verbose description of the automatic scaling rule\.  
*Required*: No  
*Type*: String

`Name`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-name"></a>
The name used to identify an automatic scaling rule\. Rule names must be unique within a scaling policy\.  
*Required*: Yes  
*Type*: String

`Trigger`  <a name="cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-trigger"></a>
The CloudWatch alarm definition that determines when automatic scaling activity is triggered\.  
*Required*: Yes  
*Type:* [Amazon EMR Cluster ScalingTrigger](aws-properties-elasticmapreduce-cluster-scalingtrigger.md)