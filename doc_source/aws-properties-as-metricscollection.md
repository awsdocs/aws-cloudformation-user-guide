# AWS::AutoScaling::AutoScalingGroup MetricsCollection<a name="aws-properties-as-metricscollection"></a>

 `MetricsCollection` is a property of the [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource that describes the group metrics that an Amazon EC2 Auto Scaling group sends to Amazon CloudWatch\. These metrics describe the group rather than any of its instances\. 

For more information, see [Monitor CloudWatch metrics for your Auto Scaling groups and instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-monitoring.html) in the *Amazon EC2 Auto Scaling User Guide*\. You can find a sample template snippet in the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#aws-properties-as-group--examples) section of the `AWS::AutoScaling::AutoScalingGroup` resource\.

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
  [Granularity](#cfn-as-metricscollection-granularity): String
  [Metrics](#cfn-as-metricscollection-metrics): 
    - String
```

## Properties<a name="aws-properties-as-metricscollection-properties"></a>

`Granularity`  <a name="cfn-as-metricscollection-granularity"></a>
The frequency at which Amazon EC2 Auto Scaling sends aggregated data to CloudWatch\. The only valid value is `1Minute`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metrics`  <a name="cfn-as-metricscollection-metrics"></a>
Identifies the metrics to enable\.  
You can specify one or more of the following metrics:  
+  `GroupMinSize` 
+  `GroupMaxSize` 
+  `GroupDesiredCapacity` 
+  `GroupInServiceInstances` 
+  `GroupPendingInstances` 
+  `GroupStandbyInstances` 
+  `GroupTerminatingInstances` 
+  `GroupTotalInstances` 
+  `GroupInServiceCapacity` 
+  `GroupPendingCapacity` 
+  `GroupStandbyCapacity` 
+  `GroupTerminatingCapacity` 
+  `GroupTotalCapacity` 
+  `WarmPoolDesiredCapacity` 
+  `WarmPoolWarmedCapacity` 
+  `WarmPoolPendingCapacity` 
+  `WarmPoolTerminatingCapacity` 
+  `WarmPoolTotalCapacity` 
+  `GroupAndWarmPoolDesiredCapacity` 
+  `GroupAndWarmPoolTotalCapacity` 
If you specify `Granularity` and don't specify any metrics, all metrics are enabled\.  
For more information, see [Auto Scaling group metrics](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-cloudwatch-monitoring.html#as-group-metrics) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)