# Amazon EMR Cluster SimpleScalingPolicyConfiguration<a name="aws-properties-elasticmapreduce-cluster-simplescalingpolicyconfiguration"></a>

`SimpleScalingPolicyConfiguration` is a subproperty of the [Amazon EMR Cluster ScalingAction](aws-properties-elasticmapreduce-cluster-scalingaction.md) property\. It specifies an automatic scaling configuration that describes how the policy adds or removes instances, the cooldown period, and the number of Amazon EC2 instances that will be added each time the CloudWatch metric alarm condition is satisfied\.

## Syntax<a name="w3ab2c21c14d946b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-cluster-simplescalingpolicyconfiguration-syntax.json"></a>

```
{
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-simplescalingpolicyconfiguration-adjustmenttype)" : String,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-simplescalingpolicyconfiguration-cooldown)" : Integer,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-simplescalingpolicyconfiguration-scalingadjustment)" : String
 }
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-simplescalingpolicyconfiguration-syntax.yaml"></a>

```
   [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-simplescalingpolicyconfiguration-adjustmenttype): String
   [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-simplescalingpolicyconfiguration-cooldown): Integer
   [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-simplescalingpolicyconfiguration-scalingadjustment): String
```

## Properties<a name="w3ab2c21c14d946b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [SimpleScalingPolicyConfiguration](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_SimpleScalingPolicyConfiguration.html) data type in the *Amazon EMR API Reference*\.

`AdjustmentType`  
The way in which Amazon EC2 instances are added \(if `ScalingAdjustment` is a positive number\) or terminated \(if `ScalingAdjustment` is a negative number\) each time the scaling activity is triggered\. `CHANGE_IN_CAPACITY` is the default\.  
*Required: *No  
*Type*: String

`CoolDown`  
The amount of time, in seconds, after a scaling activity completes before any further trigger\-related scaling activities can start\. The default value is 0\.  
*Required: *No  
*Type*: Integer

`ScalingAdjustment`  
The amount by which to scale in or scale out, based on the specified `AdjustmentType`\. A positive value adds to the instance group's Amazon EC2 instance count while a negative number removes instances\. If `AdjustmentType` is set to `EXACT_CAPACITY`, the number should only be a positive integer\. If `AdjustmentType` is set to `PERCENT_CHANGE_IN_CAPACITY`, the value should express the percentage as a decimal\.  
*Required: *Yes  
*Type*: Integer