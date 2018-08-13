# AWS Auto Scaling ScalingPlan PredefinedScalingMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification"></a>

<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-description"></a>The `PredefinedScalingMetricSpecification` property type specifies a predefined metric for a target tracking policy for an AWS Auto Scaling scaling plan\.

<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-inheritance"></a> `PredefinedScalingMetricSpecification` is a property of the [AWS Auto Scaling ScalingPlan TargetTrackingConfiguration](aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.md) property type\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-syntax.json"></a>

```
{
  "[ResourceLabel](#cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-resourcelabel)" : String,
  "[PredefinedScalingMetricType](#cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-predefinedscalingmetrictype)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-syntax.yaml"></a>

```
[ResourceLabel](#cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-resourcelabel): String
[PredefinedScalingMetricType](#cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-predefinedscalingmetrictype): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-properties"></a>

`PredefinedScalingMetricType`  <a name="cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-predefinedscalingmetrictype"></a>
The metric type\. For more information, see [PredefinedScalingMetricSpecification](http://docs.aws.amazon.com/autoscaling/plans/APIReference/API_.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResourceLabel`  <a name="cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 