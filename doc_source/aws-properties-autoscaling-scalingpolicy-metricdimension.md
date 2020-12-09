# AWS::AutoScaling::ScalingPolicy MetricDimension<a name="aws-properties-autoscaling-scalingpolicy-metricdimension"></a>

 `MetricDimension` is a subproperty of [CustomizedMetricSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-customizedmetricspecification.html) that specifies the dimensions of a metric for a target tracking scaling policy\. Dimensions are arbitrary name/value pairs that can be associated with a CloudWatch metric\. Duplicate dimensions are not allowed\. 

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-metricdimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-metricdimension-syntax.json"></a>

```
{
  "[Name](#cfn-autoscaling-scalingpolicy-metricdimension-name)" : String,
  "[Value](#cfn-autoscaling-scalingpolicy-metricdimension-value)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-metricdimension-syntax.yaml"></a>

```
  [Name](#cfn-autoscaling-scalingpolicy-metricdimension-name): String
  [Value](#cfn-autoscaling-scalingpolicy-metricdimension-value): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-metricdimension-properties"></a>

`Name`  <a name="cfn-autoscaling-scalingpolicy-metricdimension-name"></a>
The name of the dimension\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-autoscaling-scalingpolicy-metricdimension-value"></a>
The value of the dimension\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)