# Application Auto Scaling ScalingPolicy PredefinedMetricSpecification<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification"></a>

Use the `PredefinedMetricSpecification` property to configure a predefined metric for a target tracking policy to use with Application Auto Scaling\. `PredefinedMetricSpecification` is a subproperty of the [Application Auto Scaling ScalingPolicy TargetTrackingScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.md) property\.

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

For more information about each property, including constraints and valid values, see [PredefinedMetricSpecification](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PredefinedMetricSpecification.html) in the *Application Auto Scaling API Reference*\.

`PredefinedMetricType`  <a name="cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype"></a>
The metric type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ResourceLabel`  <a name="cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\. You can't specify a resource label unless the metric type is `ALBRequestCountPerTarget` and there is a target group attached to the Spot fleet request or ECS service\.  
The format is app/<load\-balancer\-name>/<load\-balancer\-id>/targetgroup/<target\-group\-name>/<target\-group\-id>, where:  
+ app/<load\-balancer\-name>/<load\-balancer\-id> is the final portion of the load balancer ARN
+ targetgroup/<target\-group\-name>/<target\-group\-id> is the final portion of the target group ARN\.
*Required*: No  
*Type*: String  
*Length constraints*: Minimum length of 1\. Maximum length of 1023\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)