# Auto Scaling ScalingPolicy PredefinedMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification"></a>

The `PredefinedMetricSpecification` property configures a predefined metric for a target tracking policy in Auto Scaling\. `PredefinedMetricSpecification` is a subproperty of the [Auto Scaling ScalingPolicy TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md) property\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-properties"></a>

For more information about each property, including constraints and valid values, see [PredefinedMetricSpecification](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_PredefinedMetricSpecification.html) in the *Auto Scaling API Reference*\.

`PredefinedMetricType`  
The metric type\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`ResourceLabel`  
Identifies the resource associated with the metric type\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption