# Amazon EMR InstanceGroupConfig ScalingRule<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingrule"></a>

The `ScalingRule` property type represents a scale\-in or scale\-out rule that defines scaling activity, including the CloudWatch metric alarm that triggers activity, how EC2 instances are added or removed, and the periodicity of adjustments\. The `Rules` subproperty of the [Amazon EMR InstanceGroupConfig AutoScalingPolicy](aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy.md) property contains a list of one or more `ScalingRule` property types\.

## Syntax<a name="w3ab2c21c14e1001b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingrule-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-action)" : ScalingAction,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-description)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-trigger)" : ScalingTrigger
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingrule-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-action): ScalingAction
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-scalingrule-trigger): ScalingTrigger
```

## Properties<a name="w3ab2c21c14e1001b7"></a>

`Action`  
The conditions that trigger an automatic scaling activity\.  
*Required: *Yes  
*Type*: [Amazon EMR InstanceGroupConfig ScalingAction](aws-properties-elasticmapreduce-instancegroupconfig-scalingaction.md)

`Description`  
A friendly, more verbose description of the automatic scaling rule\.  
*Required: *No  
*Type*: String

`Name`  
The identifier of the automatic scaling rule\. Rule names must be unique within a scaling policy\.  
*Required: *Yes  
*Type*: String

`Trigger`  
The CloudWatch alarm definition that determines when automatic scaling activity is triggered\.  
*Required: *Yes  
*Type*: [Amazon EMR InstanceGroupConfig ScalingTrigger](aws-properties-elasticmapreduce-instancegroupconfig-scalingtrigger.md)