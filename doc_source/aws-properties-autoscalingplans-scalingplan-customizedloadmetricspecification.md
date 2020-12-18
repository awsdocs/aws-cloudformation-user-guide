# AWS::AutoScalingPlans::ScalingPlan CustomizedLoadMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification"></a>

 `CustomizedLoadMetricSpecification` is a subproperty of [ScalingInstruction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-scalinginstruction.html) that specifies a customized load metric for predictive scaling to use with AWS Auto Scaling\.

For predictive scaling to work with a customized load metric specification, AWS Auto Scaling needs access to the `Sum` and `Average` statistics that CloudWatch computes from metric data\.

When you choose a load metric, make sure that the required `Sum` and `Average` statistics for your metric are available in CloudWatch and that they provide relevant data for predictive scaling\. The `Sum` statistic must represent the total load on the resource, and the `Average` statistic must represent the average load per capacity unit of the resource\. For example, there is a metric that counts the number of requests processed by your Auto Scaling group\. If the `Sum` statistic represents the total request count processed by the group, then the `Average` statistic for the specified metric must represent the average request count processed by each instance of the group\. 

If you publish your own metrics, you can aggregate the data points at a given interval and then publish the aggregated data points to CloudWatch\. Before AWS Auto Scaling generates the forecast, it sums up all the metric data points that occurred within each hour to match the granularity period that is used in the forecast \(60 minutes\)\.

For information about terminology, available metrics, or how to publish new metrics, see [Amazon CloudWatch Concepts](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html) in the *Amazon CloudWatch User Guide*\. 

After creating your scaling plan, you can use the AWS Auto Scaling console to visualize forecasts for the specified metric\. For more information, see [View Scaling Information for a Resource](https://docs.aws.amazon.com/autoscaling/plans/userguide/gs-create-scaling-plan.html#gs-view-resource) in the *AWS Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax.json"></a>

```
{
  "[Dimensions](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-dimensions)" : [ MetricDimension, ... ],
  "[MetricName](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-metricname)" : String,
  "[Namespace](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-namespace)" : String,
  "[Statistic](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-statistic)" : String,
  "[Unit](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification-syntax.yaml"></a>

```
  [Dimensions](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-dimensions): 
    - MetricDimension
  [MetricName](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-metricname): String
  [Namespace](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-namespace): String
  [Statistic](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-statistic): String
  [Unit](#cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit): String
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
The statistic of the metric\.  
*Allowed Values*: `Sum`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-autoscalingplans-scalingplan-customizedloadmetricspecification-unit"></a>
The unit of the metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-autoscalingplans-scalingplan-customizedloadmetricspecification--seealso"></a>
+ [AWS Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/plans/userguide/what-is-aws-auto-scaling.html)