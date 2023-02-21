# AWS::AutoScaling::ScalingPolicy PredictiveScalingConfiguration<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingconfiguration"></a>

 `PredictiveScalingConfiguration` is a property of the [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html) resource that specifies a predictive scaling policy for Amazon EC2 Auto Scaling\. 

For more information, see [Predictive scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-predictive-scaling.html) in the *Amazon EC2 Auto Scaling User Guide*\. 

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingconfiguration-syntax.json"></a>

```
{
  "[MaxCapacityBreachBehavior](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-maxcapacitybreachbehavior)" : String,
  "[MaxCapacityBuffer](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-maxcapacitybuffer)" : Integer,
  "[MetricSpecifications](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-metricspecifications)" : [ PredictiveScalingMetricSpecification, ... ],
  "[Mode](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-mode)" : String,
  "[SchedulingBufferTime](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-schedulingbuffertime)" : Integer
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingconfiguration-syntax.yaml"></a>

```
  [MaxCapacityBreachBehavior](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-maxcapacitybreachbehavior): String
  [MaxCapacityBuffer](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-maxcapacitybuffer): Integer
  [MetricSpecifications](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-metricspecifications): 
    - PredictiveScalingMetricSpecification
  [Mode](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-mode): String
  [SchedulingBufferTime](#cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-schedulingbuffertime): Integer
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingconfiguration-properties"></a>

`MaxCapacityBreachBehavior`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-maxcapacitybreachbehavior"></a>
Defines the behavior that should be applied if the forecast capacity approaches or exceeds the maximum capacity of the Auto Scaling group\. Defaults to `HonorMaxCapacity` if not specified\.  
The following are possible values:  
+  `HonorMaxCapacity` \- Amazon EC2 Auto Scaling cannot scale out capacity higher than the maximum capacity\. The maximum capacity is enforced as a hard limit\. 
+  `IncreaseMaxCapacity` \- Amazon EC2 Auto Scaling can scale out capacity higher than the maximum capacity when the forecast capacity is close to or exceeds the maximum capacity\. The upper limit is determined by the forecasted capacity and the value for `MaxCapacityBuffer`\.
*Required*: No  
*Type*: String  
*Allowed values*: `HonorMaxCapacity | IncreaseMaxCapacity`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxCapacityBuffer`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-maxcapacitybuffer"></a>
The size of the capacity buffer to use when the forecast capacity is close to or exceeds the maximum capacity\. The value is specified as a percentage relative to the forecast capacity\. For example, if the buffer is 10, this means a 10 percent buffer, such that if the forecast capacity is 50, and the maximum capacity is 40, then the effective maximum capacity is 55\.  
If set to 0, Amazon EC2 Auto Scaling may scale capacity higher than the maximum capacity to equal but not exceed forecast capacity\.   
Required if the `MaxCapacityBreachBehavior` property is set to `IncreaseMaxCapacity`, and cannot be used otherwise\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricSpecifications`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-metricspecifications"></a>
This structure includes the metrics and target utilization to use for predictive scaling\.   
This is an array, but we currently only support a single metric specification\. That is, you can specify a target value and a single metric pair, or a target value and one scaling metric and one load metric\.  
*Required*: Yes  
*Type*: List of [PredictiveScalingMetricSpecification](aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mode`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-mode"></a>
The predictive scaling mode\. Defaults to `ForecastOnly` if not specified\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ForecastAndScale | ForecastOnly`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchedulingBufferTime`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingconfiguration-schedulingbuffertime"></a>
The amount of time, in seconds, by which the instance launch time can be advanced\. For example, the forecast says to add capacity at 10:00 AM, and you choose to pre\-launch instances by 5 minutes\. In that case, the instances will be launched at 9:55 AM\. The intention is to give resources time to be provisioned\. It can take a few minutes to launch an EC2 instance\. The actual amount of time required depends on several factors, such as the size of the instance and whether there are startup scripts to complete\.   
The value must be less than the forecast interval duration of 3600 seconds \(60 minutes\)\. Defaults to 300 seconds if not specified\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)