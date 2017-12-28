# Amazon EMR Cluster ScalingAction<a name="aws-properties-elasticmapreduce-cluster-scalingaction"></a>

The `ScalingAction` property type specifies the scaling actions for an Auto Scaling group policy\. `ScalingAction` is the property type for the `Action` subproperty of the [Amazon EMR Cluster ScalingRule](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule.md) property type\.

## Syntax<a name="w3ab2c21c14d922b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-cluster-scalingaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingaction-market)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingaction-simplescalingpolicyconfiguration)" : SimpleScalingPolicyConfiguration
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-scalingaction-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingaction-market): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingaction-simplescalingpolicyconfiguration): SimpleScalingPolicyConfiguration
```

## Properties<a name="w3ab2c21c14d922b7"></a>

`Market`  
Not available for instance groups\. Instance groups use the market type specified for the group\.  
Valid values: `ON_DEMAND` or `SPOT`  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`SimpleScalingPolicyConfiguration`  
The type of adjustment the automatic scaling activity makes when triggered, and the periodicity of the adjustment\.  
*Required: *Yes  
*Type*: [Amazon EMR Cluster SimpleScalingPolicyConfiguration](aws-properties-elasticmapreduce-cluster-simplescalingpolicyconfiguration.md)  
*Update requires*: No interruption