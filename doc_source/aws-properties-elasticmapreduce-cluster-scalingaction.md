# Amazon EMR Cluster ScalingAction<a name="aws-properties-elasticmapreduce-cluster-scalingaction"></a>

The `ScalingAction` property type specifies the scaling actions for an Auto Scaling group policy\. `ScalingAction` is the property type for the `Action` subproperty of the [Amazon EMR Cluster ScalingRule](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule.md) property type\.

## Syntax<a name="w3ab2c21c14e1113b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-cluster-scalingaction-syntax.json"></a>

```
{
  "[Market](#cfn-elasticmapreduce-cluster-scalingaction-market)" : String,
  "[SimpleScalingPolicyConfiguration](#cfn-elasticmapreduce-cluster-scalingaction-simplescalingpolicyconfiguration)" : SimpleScalingPolicyConfiguration
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-scalingaction-syntax.yaml"></a>

```
  [Market](#cfn-elasticmapreduce-cluster-scalingaction-market): String
  [SimpleScalingPolicyConfiguration](#cfn-elasticmapreduce-cluster-scalingaction-simplescalingpolicyconfiguration): SimpleScalingPolicyConfiguration
```

## Properties<a name="w3ab2c21c14e1113b7"></a>

`Market`  <a name="cfn-elasticmapreduce-cluster-scalingaction-market"></a>
Not available for instance groups\. Instance groups use the market type specified for the group\.  
Valid values: `ON_DEMAND` or `SPOT`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SimpleScalingPolicyConfiguration`  <a name="cfn-elasticmapreduce-cluster-scalingaction-simplescalingpolicyconfiguration"></a>
The type of adjustment the automatic scaling activity makes when triggered, and the periodicity of the adjustment\.  
*Required*: Yes  
*Type*: [Amazon EMR Cluster SimpleScalingPolicyConfiguration](aws-properties-elasticmapreduce-cluster-simplescalingpolicyconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)