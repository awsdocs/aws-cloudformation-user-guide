# AWS Auto Scaling ScalingPlan PredefinedLoadMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification"></a>

<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-description"></a>The `PredefinedLoadMetricSpecification` property type specifies a predefined load metric for predictive scaling to use with AWS Auto Scaling\.

<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-inheritance"></a> `PredefinedLoadMetricSpecification` is a property of the [ScalingInstruction](aws-properties-autoscalingplans-scalingplan-scalinginstruction.md) property type\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-syntax.json"></a>

```
{
  "[PredefinedLoadMetricType](#cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-predefinedloadmetrictype)" : String,
  "[ResourceLabel](#cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-syntax.yaml"></a>

```
[PredefinedLoadMetricType](#cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-predefinedloadmetrictype): String
[ResourceLabel](#cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-properties"></a>

`PredefinedLoadMetricType`  <a name="cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-predefinedloadmetrictype"></a>
The metric type\. For more information, see [PredefinedLoadMetricSpecification](https://docs.aws.amazon.com/autoscaling/plans/APIReference/API_PredefinedLoadMetricSpecification.html) in the *AWS Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResourceLabel`  <a name="cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\. You can't specify a resource label unless the metric type is `ALBRequestCountPerTarget` and there is a target group for an Application Load Balancer attached to the Auto Scaling group\.  
The format is app/<load\-balancer\-name>/<load\-balancer\-id>/targetgroup/<target\-group\-name>/<target\-group\-id>, where:  
+ app/<load\-balancer\-name>/<load\-balancer\-id> is the final portion of the load balancer ARN\.
+ targetgroup/<target\-group\-name>/<target\-group\-id> is the final portion of the target group ARN\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 