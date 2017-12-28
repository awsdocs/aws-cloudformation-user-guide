# Amazon EMR Cluster ScalingRule<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule"></a>

The `ScalingRule` property type represents a scale\-in or scale\-out rule that defines scaling activity, including the CloudWatch metric alarm that triggers activity, how Amazon EC2 instances are added or removed, and the periodicity of adjustments\. The `Rules` subproperty of the [Amazon EMR Cluster JobFlowInstancesConfig](aws-properties-emr-cluster-jobflowinstancesconfig.md) property contains a list of one or more `ScalingRule` property types\.

## Syntax<a name="w3ab2c21c14d930b5"></a>

### JSON<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-action)" : ScalingAction,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-description)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-trigger)" : ScalingTrigger
}
```

### YAML<a name="aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-action): ScalingAction
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-trigger): ScalingTrigger
```

## Properties<a name="w3ab2c21c14d930b7"></a>

`Action`  
The conditions that trigger an automatic scaling activity\.  
*Required: *Yes  
*Type:* [Amazon EMR Cluster ScalingAction](aws-properties-elasticmapreduce-cluster-scalingaction.md)

`Description`  
A friendly, more verbose description of the automatic scaling rule\.  
*Required: *No  
*Type*: String

`Name`  
The name used to identify an automatic scaling rule\. Rule names must be unique within a scaling policy\.  
*Required: *Yes  
*Type*: String

`Trigger`  
The CloudWatch alarm definition that determines when automatic scaling activity is triggered\.  
*Required: *Yes  
*Type:* [Amazon EMR Cluster ScalingTrigger](aws-properties-elasticmapreduce-cluster-scalingtrigger.md)