# Application Auto Scaling ScalingPolicy CustomizedMetricSpecification<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification"></a>

The `CustomizedMetricSpecification` property configures a customized metric for a target tracking policy in Application Auto Scaling\. `CustomizedMetricSpecification` is a subproperty of the [Application Auto Scaling ScalingPolicy TargetTrackingScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.md) property\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions)" : [ MetricDimension, ...],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-dimensions):
  - MetricDimension
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-metricname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-namespace): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-statistic): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-applicationautoscaling-scalingpolicy-customizedmetricspecification-unit): String
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-customizedmetricspecification-properties"></a>

`Dimensions`  
The dimensions of the metric\. Duplicates not allowed\.  
*Required: *No  
*Type*: List of [Application Auto Scaling ScalingPolicy MetricDimension](aws-properties-applicationautoscaling-scalingpolicy-metricdimension.md)  
*Update requires*: No interruption

`MetricName`  
The name of the metric\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Namespace`  
The namespace of the metric\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Statistic`  
The statistic of the metric\.  
For valid values, see [CustomizedMetricSpecification](http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_CustomizedMetricSpecification.html) in the *Application Auto Scaling API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Unit`  
The unit of the metric\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption