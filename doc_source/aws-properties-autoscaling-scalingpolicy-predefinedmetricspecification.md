# Amazon EC2 Auto Scaling ScalingPolicy PredefinedMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification"></a>

The `PredefinedMetricSpecification` property configures a predefined metric for a target tracking policy in Amazon EC2 Auto Scaling\. `PredefinedMetricSpecification` is a subproperty of the [Amazon EC2 Auto Scaling ScalingPolicy TargetTrackingConfiguration](aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.md) property\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax.json"></a>

```
{
  "[PredefinedMetricType](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype)" : String,
  "[ResourceLabel](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax.yaml"></a>

```
[PredefinedMetricType](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype): String
[ResourceLabel](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-properties"></a>

For more information about each property, including constraints and valid values, see [PredefinedMetricSpecification](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PredefinedMetricSpecification.html) in the *Amazon EC2 Auto Scaling API Reference*\.

`PredefinedMetricType`  <a name="cfn-autoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype"></a>
The metric type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ResourceLabel`  <a name="cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)