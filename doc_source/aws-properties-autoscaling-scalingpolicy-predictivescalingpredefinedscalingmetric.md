# AWS::AutoScaling::ScalingPolicy PredictiveScalingPredefinedScalingMetric<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric"></a>

Contains scaling metric information for the `PredefinedScalingMetricSpecification` property of the [AWS::AutoScaling::ScalingPolicy PredictiveScalingMetricSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification.html) property type\.

**Important**  
Does not apply to policies that use a *metric pair* for the metric specification\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-syntax.json"></a>

```
{
  "[PredefinedMetricType](#cfn-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-predefinedmetrictype)" : String,
  "[ResourceLabel](#cfn-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-syntax.yaml"></a>

```
  [PredefinedMetricType](#cfn-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-predefinedmetrictype): String
  [ResourceLabel](#cfn-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-resourcelabel): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-properties"></a>

`PredefinedMetricType`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-predefinedmetrictype"></a>
The metric type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALBRequestCountPerTarget | ASGAverageCPUUtilization | ASGAverageNetworkIn | ASGAverageNetworkOut`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLabel`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingpredefinedscalingmetric-resourcelabel"></a>
A label that uniquely identifies a specific Application Load Balancer target group from which to determine the average request count served by your Auto Scaling group\. You can't specify a resource label unless the target group is attached to the Auto Scaling group\.  
You create the resource label by appending the final portion of the load balancer ARN and the final portion of the target group ARN into a single value, separated by a forward slash \(/\)\. The format of the resource label is:  
 `app/my-alb/778d41231b141a0f/targetgroup/my-alb-target-group/943f017f100becff`\.  
Where:  
+ app/<load\-balancer\-name>/<load\-balancer\-id> is the final portion of the load balancer ARN
+ targetgroup/<target\-group\-name>/<target\-group\-id> is the final portion of the target group ARN\.
To find the ARN for an Application Load Balancer, use the [DescribeLoadBalancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_DescribeLoadBalancers.html) API operation\. To find the ARN for the target group, use the [DescribeTargetGroups](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_DescribeTargetGroups.html) API operation\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)