# Auto Scaling ScalingPolicy CustomizedMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification"></a>

The `CustomizedMetricSpecification` property configures a customized metric for a target tracking policy in Auto Scaling\. `CustomizedMetricSpecification` is a subproperty of the [Auto Scaling ScalingPolicy TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md) property\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions)" : [ MetricDimension, ...],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions):
  - MetricDimension
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-properties"></a>

`Dimensions`  
The dimensions of the metric\. Duplicates not allowed\.  
*Required: *No  
*Type*: List of [Auto Scaling ScalingPolicy MetricDimension](aws-properties-autoscaling-scalingpolicy-metricdimension.md)  
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
For valid values, see [CustomizedMetricSpecification](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_CustomizedMetricSpecification.html) in the *Auto Scaling API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Unit`  
The unit of the metric\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption