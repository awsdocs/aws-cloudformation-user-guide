# AWS::AutoScaling::AutoScalingGroup MetricsCollection<a name="aws-properties-as-metricscollection"></a>

 `MetricsCollection` is a property of [AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) that describes the group metrics that an Amazon EC2 Auto Scaling group sends to Amazon CloudWatch\. These metrics describe the group rather than any of its instances\. 

For more information, see [Monitoring Your Auto Scaling Groups and Instances Using Amazon CloudWatch](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-monitoring.html) in the *Amazon EC2 Auto Scaling User Guide*\. 

## Syntax<a name="aws-properties-as-metricscollection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-metricscollection-syntax.json"></a>

```
{
  "[Granularity](#cfn-as-metricscollection-granularity)" : String,
  "[Metrics](#cfn-as-metricscollection-metrics)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-as-metricscollection-syntax.yaml"></a>

```
﻿  [Granularity](#cfn-as-metricscollection-granularity) : String
﻿  [Metrics](#cfn-as-metricscollection-metrics) : 
    - String
```

## Properties<a name="aws-properties-as-metricscollection-properties"></a>

`Granularity`  <a name="cfn-as-metricscollection-granularity"></a>
The frequency at which Amazon EC2 Auto Scaling sends aggregated data to CloudWatch\. The only valid value is `1Minute`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metrics`  <a name="cfn-as-metricscollection-metrics"></a>
The list of Auto Scaling group metrics to collect\. If you specify `Granularity` and don't specify any metrics, all metrics are enabled\.   
+ `GroupMinSize`
+ `GroupMaxSize`
+ `GroupDesiredCapacity`
+ `GroupInServiceInstances`
+ `GroupPendingInstances`
+ `GroupStandbyInstances`
+ `GroupTerminatingInstances`
+ `GroupTotalInstances`
*Required*: No  
*Type*: List of String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)