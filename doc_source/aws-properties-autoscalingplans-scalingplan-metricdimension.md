# AWS::AutoScalingPlans::ScalingPlan MetricDimension<a name="aws-properties-autoscalingplans-scalingplan-metricdimension"></a>

 `MetricDimension` is a subproperty of [CustomizedScalingMetricSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-customizedscalingmetricspecification.html) that specifies a dimension for a customized metric to use with AWS Auto Scaling\. Dimensions are arbitrary name/value pairs that can be associated with a CloudWatch metric\. Duplicate dimensions are not allowed\. 

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-syntax.json"></a>

```
{
  "[Name](#cfn-autoscalingplans-scalingplan-metricdimension-name)" : String,
  "[Value](#cfn-autoscalingplans-scalingplan-metricdimension-value)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-syntax.yaml"></a>

```
  [Name](#cfn-autoscalingplans-scalingplan-metricdimension-name): String
  [Value](#cfn-autoscalingplans-scalingplan-metricdimension-value): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-metricdimension-properties"></a>

`Name`  <a name="cfn-autoscalingplans-scalingplan-metricdimension-name"></a>
The name of the dimension\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-autoscalingplans-scalingplan-metricdimension-value"></a>
The value of the dimension\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)