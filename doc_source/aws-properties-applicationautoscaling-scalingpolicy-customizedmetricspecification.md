# AWS::ApplicationAutoScaling::ScalingPolicy CustomizedMetricSpecification<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification"></a>

 `CustomizedMetricSpecification` is a subproperty of [TargetTrackingScalingPolicyConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.html) that configures a customized metric for a target tracking scaling policy to use with Application Auto Scaling\. 

For more information, see [CustomizedMetricSpecification](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_CustomizedMetricSpecification.html) in the *Application Auto Scaling API Reference*\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions)" : [ MetricDimension, ... ],
  "[MetricName](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname)" : String,
  "[Namespace](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace)" : String,
  "[Statistic](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic)" : String,
  "[Unit](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax.yaml"></a>

```
  [Dimensions](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions): 
    - MetricDimension
  [MetricName](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname): String
  [Namespace](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace): String
  [Statistic](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic): String
  [Unit](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit): String
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions"></a>
The dimensions of the metric\.   
Conditional: If you published your metric with dimensions, you must specify the same dimensions in your scaling policy\.  
*Required*: No  
*Type*: List of [MetricDimension](aws-properties-applicationautoscaling-scalingpolicy-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname"></a>
The name of the metric\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic"></a>
The statistic of the metric\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Average | Maximum | Minimum | SampleCount | Sum`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit"></a>
The unit of the metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification--seealso"></a>
+ [Target tracking scaling policies](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html) in the *Application Auto Scaling User Guide*

