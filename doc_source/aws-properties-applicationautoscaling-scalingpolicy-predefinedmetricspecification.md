# Application Auto Scaling ScalingPolicy PredefinedMetricSpecification<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification"></a>

Use the `PredefinedMetricSpecification` property to configure a predefined metric for a target tracking policy in Application Auto Scaling\. `PredefinedMetricSpecification` is a subproperty of the [Application Auto Scaling ScalingPolicy TargetTrackingScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.md) property\.

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax.json"></a>

```
{
  "[PredefinedMetricType](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype)" : String,
  "[ResourceLabel](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax.yaml"></a>

```
[PredefinedMetricType](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype): String
[ResourceLabel](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-properties"></a>

For more information about each property, including constraints and valid values, see [PredefinedMetricSpecification](http://docs.aws.amazon.com/autoscaling/application/APIReference/API_PredefinedMetricSpecification.html) in the *Application Auto Scaling API Reference*\.

`PredefinedMetricType`  <a name="cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype"></a>
The metric type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ResourceLabel`  <a name="cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel"></a>
This property is reserved for future use\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)