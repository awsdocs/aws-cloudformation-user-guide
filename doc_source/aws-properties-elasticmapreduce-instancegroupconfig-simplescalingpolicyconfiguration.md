# Amazon EMR InstanceGroupConfig SimpleScalingPolicyConfiguration<a name="aws-properties-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration"></a>

`SimpleScalingPolicyConfiguration` specifies an automatic scaling configuration that describes how the policy adds or removes instances, the cooldown period, and the number of EC2 instances that are added when the CloudWatch metric alarm condition is met\. `SimpleScalingPolicyConfiguration` is a subproperty of the [Amazon EMR InstanceGroupConfig ScalingAction](aws-properties-elasticmapreduce-instancegroupconfig-scalingaction.md) property type\.

## Syntax<a name="w3ab2c21c14e1197b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-syntax.json"></a>

```
{
  "[AdjustmentType](#cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-adjustmenttype)" : String,
  "[CoolDown](#cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-cooldown)" : Integer,
  "[ScalingAdjustment](#cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-scalingadjustment)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-syntax.yaml"></a>

```
  [AdjustmentType](#cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-adjustmenttype): String
  [CoolDown](#cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-cooldown): Integer
  [ScalingAdjustment](#cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-scalingadjustment): String
```

## Properties<a name="w3ab2c21c14e1197b7"></a>

**Note**  
For more information about each property, including constraints and valid values, see [SimpleScalingPolicyConfiguration](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_SimpleScalingPolicyConfiguration.html) in the *Amazon EMR API Reference*\.

`AdjustmentType`  <a name="cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-adjustmenttype"></a>
The way in which EC2 instances are added \(if `ScalingAdjustment` is a positive number\) or terminated \(if `ScalingAdjustment` is a negative number\) when the scaling activity is triggered\. `CHANGE_IN_CAPACITY` is the default value\.  
*Required*: No  
*Type*: String

`CoolDown`  <a name="cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-cooldown"></a>
The amount of time, in seconds, after a scaling activity completes before any further trigger\-related scaling activities can start\. The default value is 0\.  
*Required*: No  
*Type*: Integer

`ScalingAdjustment`  <a name="cfn-elasticmapreduce-instancegroupconfig-simplescalingpolicyconfiguration-scalingadjustment"></a>
The amount by which to scale the instance group, based on the specified `AdjustmentType`\. A positive value adds to the instance group's EC2 instance count\. A negative number removes instances\. If `AdjustmentType` is set to `EXACT_CAPACITY`, specify only a positive integer\. If `AdjustmentType` is set to `PERCENT_CHANGE_IN_CAPACITY`, express the value of the percentage as a decimal\. For example, `-0.20` indicates a decrease in 20% increments of cluster capacity\.  
*Required*: Yes  
*Type*: Integer