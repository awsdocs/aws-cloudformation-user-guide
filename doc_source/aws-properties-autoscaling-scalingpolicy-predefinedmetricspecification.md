# AWS::AutoScaling::ScalingPolicy PredefinedMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification"></a>

Contains predefined metric specification information for a target tracking scaling policy for Amazon EC2 Auto Scaling\.

 `PredefinedMetricSpecification` is a property of the [AWS::AutoScaling::ScalingPolicy TargetTrackingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.html) property type\.

## Syntax<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax.json"></a>

```
{
  "[PredefinedMetricType](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype)" : String,
  "[ResourceLabel](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-syntax.yaml"></a>

```
  [PredefinedMetricType](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype): String
  [ResourceLabel](#cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification-properties"></a>

`PredefinedMetricType`  <a name="cfn-autoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype"></a>
The metric type\. The following predefined metrics are available:  
+  `ASGAverageCPUUtilization` \- Average CPU utilization of the Auto Scaling group\.
+  `ASGAverageNetworkIn` \- Average number of bytes received on all network interfaces by the Auto Scaling group\.
+  `ASGAverageNetworkOut` \- Average number of bytes sent out on all network interfaces by the Auto Scaling group\.
+  `ALBRequestCountPerTarget` \- Average Application Load Balancer request count per target for your Auto Scaling group\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALBRequestCountPerTarget | ASGAverageCPUUtilization | ASGAverageNetworkIn | ASGAverageNetworkOut`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLabel`  <a name="cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel"></a>
A label that uniquely identifies a specific Application Load Balancer target group from which to determine the average request count served by your Auto Scaling group\. You can't specify a resource label unless the target group is attached to the Auto Scaling group\.  
You create the resource label by appending the final portion of the load balancer ARN and the final portion of the target group ARN into a single value, separated by a forward slash \(/\)\. The format of the resource label is:  
 `app/my-alb/778d41231b141a0f/targetgroup/my-alb-target-group/943f017f100becff`\.  
Where:  
+ app/<load\-balancer\-name>/<load\-balancer\-id> is the final portion of the load balancer ARN
+ targetgroup/<target\-group\-name>/<target\-group\-id> is the final portion of the target group ARN\.
To find the ARN for an Application Load Balancer, use the [DescribeLoadBalancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_DescribeLoadBalancers.html) API operation\. To find the ARN for the target group, use the [DescribeTargetGroups](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_DescribeTargetGroups.html) API operation\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1023`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)