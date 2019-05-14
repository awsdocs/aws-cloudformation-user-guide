# AWS::AutoScalingPlans::ScalingPlan CustomizedLoadMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification"></a>

 `CustomizedLoadMetricSpecification` is a subproperty of [ScalingInstruction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-scalinginstruction.html) that specifies a customized load metric for predictive scaling to use with AWS Auto Scaling\. 

For more information, see [CustomizedLoadMetricSpecification](https://docs.aws.amazon.com/autoscaling/plans/APIReference/API_CustomizedLoadMetricSpecification.html) in the *AWS Auto Scaling API Reference*\. 

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-dimensions)" : [ [MetricDimension](aws-properties-autoscalingplans-scalingplan-metricdimension.md), ... ],
  "[MetricName](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-metricname)" : String,
  "[Namespace](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-namespace)" : String,
  "[Statistic](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-statistic)" : String,
  "[Unit](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax.yaml"></a>

```
﻿  [Dimensions](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-dimensions) : 
    - [MetricDimension](aws-properties-autoscalingplans-scalingplan-metricdimension.md)
﻿  [MetricName](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-metricname) : String
﻿  [Namespace](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-namespace) : String
﻿  [Statistic](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-statistic) : String
﻿  [Unit](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit) : String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-dimensions"></a>
The dimensions of the metric\.  
Conditional: If you published your metric with dimensions, you must specify the same dimensions in your customized load metric specification\.  
*Required*: No  
*Type*: List of [MetricDimension](aws-properties-autoscalingplans-scalingplan-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-metricname"></a>
The name of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-statistic"></a>
The statistic of the metric\. Currently, the value must always be `Sum`\.   
*Required*: Yes  
*Type*: String  
*Allowed Values*: `Average | Maximum | Minimum | SampleCount | Sum`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit"></a>
The unit of the metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)