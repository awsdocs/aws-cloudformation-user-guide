# AWS::AutoScaling::ScalingPolicy PredefinedMetricSpecification<a name="aws-properties-autoscaling-scalingpolicy-predefinedmetricspecification"></a>

 `PredefinedMetricSpecification` is a subproperty of [TargetTrackingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-scalingpolicy-targettrackingconfiguration.html) that configures a predefined metric for a target tracking policy to use with Amazon EC2 Auto Scaling\. 

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
The metric type\. The following predefined metrics are available\.  
+  `ASGAverageCPUUtilization` \- Average CPU utilization of the Auto Scaling group\.
+  `ASGAverageNetworkIn` \- Average number of bytes received on all network interfaces by the Auto Scaling group\.
+  `ASGAverageNetworkOut` \- Average number of bytes sent out on all network interfaces by the Auto Scaling group\.
+  `ALBRequestCountPerTarget` \- Number of requests completed per target in an Application Load Balancer target group\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALBRequestCountPerTarget | ASGAverageCPUUtilization | ASGAverageNetworkIn | ASGAverageNetworkOut`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLabel`  <a name="cfn-autoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\. You can't specify a resource label unless the metric type is `ALBRequestCountPerTarget` and there is a target group attached to the Auto Scaling group\.  
The format is `app/load-balancer-name/load-balancer-id/targetgroup/target-group-name/target-group-id `, where   
+ `app/load-balancer-name/load-balancer-id ` is the final portion of the load balancer ARN, and
+ `targetgroup/target-group-name/target-group-id ` is the final portion of the target group ARN\.
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1023`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)