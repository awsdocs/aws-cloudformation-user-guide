# AWS::AutoScaling::ScalingPolicy CustomizedMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification"></a>

 `CustomizedMetricSpecification` is a subproperty of [TargetTrackingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.html) that configures a customized metric for a target tracking policy to use with Amazon EC2 Auto Scaling\. 

For more information, see [CustomizedMetricSpecification](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CustomizedMetricSpecification.html) in the *Amazon EC2 Auto Scaling API Reference*\. 

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions)" : [ MetricDimension, ... ],
  "[MetricName](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname)" : String,
  "[Namespace](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace)" : String,
  "[Statistic](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic)" : String,
  "[Unit](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-syntax.yaml"></a>

```
  [Dimensions](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions): 
    - MetricDimension
  [MetricName](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname): String
  [Namespace](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace): String
  [Statistic](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic): String
  [Unit](#cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-customizedmetricspecification-properties"></a>

`Dimensions`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-dimensions"></a>
The dimensions of the metric\.  
Conditional: If you published your metric with dimensions, you must specify the same dimensions in your scaling policy\.  
*Required*: No  
*Type*: List of [MetricDimension](aws-properties-autoscaling-scalingpolicy-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-metricname"></a>
The name of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-statistic"></a>
The statistic of the metric\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Average | Maximum | Minimum | SampleCount | Sum`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-autoscaling-scalingpolicy-customizedmetricspecification-unit"></a>
The unit of the metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)