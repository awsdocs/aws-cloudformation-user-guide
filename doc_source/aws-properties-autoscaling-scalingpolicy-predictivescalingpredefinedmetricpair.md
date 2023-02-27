# AWS::AutoScaling::ScalingPolicy PredictiveScalingPredefinedMetricPair<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair"></a>

Contains metric pair information for the `PredefinedMetricPairSpecification` property of the [AWS::AutoScaling::ScalingPolicy PredictiveScalingMetricSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-predictivescalingmetricspecification.html) property type\.

For more information, see [Predictive scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-predictive-scaling.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-syntax.json"></a>

```
{
  "[PredefinedMetricType](#cfn-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-predefinedmetrictype)" : String,
  "[ResourceLabel](#cfn-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-syntax.yaml"></a>

```
  [PredefinedMetricType](#cfn-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-predefinedmetrictype): String
  [ResourceLabel](#cfn-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-resourcelabel): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-properties"></a>

`PredefinedMetricType`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-predefinedmetrictype"></a>
Indicates which metrics to use\. There are two different types of metrics for each metric type: one is a load metric and one is a scaling metric\. For example, if the metric type is `ASGCPUUtilization`, the Auto Scaling group's total CPU metric is used as the load metric, and the average CPU metric is used for the scaling metric\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALBRequestCount | ASGCPUUtilization | ASGNetworkIn | ASGNetworkOut`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLabel`  <a name="cfn-autoscaling-scalingpolicy-predictivescalingpredefinedmetricpair-resourcelabel"></a>
A label that uniquely identifies a specific Application Load Balancer target group from which to determine the total and average request count served by your Auto Scaling group\. You can't specify a resource label unless the target group is attached to the Auto Scaling group\.  
You create the resource label by appending the final portion of the load balancer ARN and the final portion of the target group ARN into a single value, separated by a forward slash \(/\)\. The format of the resource label is:  
 `app/my-alb/778d41231b141a0f/targetgroup/my-alb-target-group/943f017f100becff`\.  
Where:  
+ app/<load\-balancer\-name>/<load\-balancer\-id> is the final portion of the load balancer ARN
+ targetgroup/<target\-group\-name>/<target\-group\-id> is the final portion of the target group ARN\.
To find the ARN for an Application Load Balancer, use the [DescribeLoadBalancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_DescribeLoadBalancers.html) API operation\. To find the ARN for the target group, use the [DescribeTargetGroups](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_DescribeTargetGroups.html) API operation\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1023`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)