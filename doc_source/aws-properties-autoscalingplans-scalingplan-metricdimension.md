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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
