# Amazon EMR InstanceGroupConfig ScalingAction<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingaction"></a>

The `ScalingAction` property type specifies the scaling actions for an Auto Scaling group policy\. `ScalingAction` is the property type for the `Action` subproperty of the [Amazon EMR InstanceGroupConfig ScalingRule](aws-properties-elasticmapreduce-instancegroupconfig-scalingrule.md) property type\.

## Syntax<a name="w3ab2c21c14e1187b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingaction-syntax.json"></a>

```
{
  "[Market](#cfn-elasticmapreduce-instancegroupconfig-scalingaction-market)" : String,
  "[SimpleScalingPolicyConfiguration](#cfn-elasticmapreduce-instancegroupconfig-scalingaction-simplescalingpolicyconfiguration)" : SimpleScalingPolicyConfiguration
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-scalingaction-syntax.yaml"></a>

```
  [Market](#cfn-elasticmapreduce-instancegroupconfig-scalingaction-market): String
  [SimpleScalingPolicyConfiguration](#cfn-elasticmapreduce-instancegroupconfig-scalingaction-simplescalingpolicyconfiguration): SimpleScalingPolicyConfiguration
```

## Properties<a name="w3ab2c21c14e1187b7"></a>

`Market`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingaction-market"></a>
Not available for instance groups\. Instance groups use the market type specified for the group\.  
Valid values: `ON_DEMAND` or `SPOT`\.  
*Required*: No  
*Type*: String

`SimpleScalingPolicyConfiguration`  <a name="cfn-elasticmapreduce-instancegroupconfig-scalingaction-simplescalingpolicyconfiguration"></a>
The type of adjustment that the automatic scaling activity makes when triggered, and the periodicity of the adjustment\.  
*Required*: Yes  
*Type*: [Amazon EMR InstanceGroupConfig SimpleScalingPolicyConfiguration](aws-properties-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration.md)