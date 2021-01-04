# AWS::AutoScalingPlans::ScalingPlan PredefinedScalingMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification"></a>

 `PredefinedScalingMetricSpecification` is a subproperty of [TargetTrackingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-targettrackingconfiguration.html) that specifies a customized scaling metric for a target tracking configuration to use with AWS Auto Scaling\. 



## Syntax<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-syntax.json"></a>

```
{
  "[PredefinedScalingMetricType](#cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-predefinedscalingmetrictype)" : String,
  "[ResourceLabel](#cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-syntax.yaml"></a>

```
  [PredefinedScalingMetricType](#cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-predefinedscalingmetrictype): String
  [ResourceLabel](#cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification-properties"></a>

`PredefinedScalingMetricType`  <a name="cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-predefinedscalingmetrictype"></a>
The metric type\. The `ALBRequestCountPerTarget` metric type applies only to Auto Scaling groups, Spot Fleet requests, and ECS services\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALBRequestCountPerTarget | ASGAverageCPUUtilization | ASGAverageNetworkIn | ASGAverageNetworkOut | DynamoDBReadCapacityUtilization | DynamoDBWriteCapacityUtilization | EC2SpotFleetRequestAverageCPUUtilization | EC2SpotFleetRequestAverageNetworkIn | EC2SpotFleetRequestAverageNetworkOut | ECSServiceAverageCPUUtilization | ECSServiceAverageMemoryUtilization | RDSReaderAverageCPUUtilization | RDSReaderAverageDatabaseConnections`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLabel`  <a name="cfn-autoscalingplans-scalingplan-predefinedscalingmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\. You can't specify a resource label unless the metric type is `ALBRequestCountPerTarget` and there is a target group for an Application Load Balancer attached to the Auto Scaling group, Spot Fleet request, or ECS service\.  
You create the resource label by appending the final portion of the load balancer ARN and the final portion of the target group ARN into a single value, separated by a forward slash \(/\)\. The format is app/<load\-balancer\-name>/<load\-balancer\-id>/targetgroup/<target\-group\-name>/<target\-group\-id>, where:  
+ app/<load\-balancer\-name>/<load\-balancer\-id> is the final portion of the load balancer ARN
+ targetgroup/<target\-group\-name>/<target\-group\-id> is the final portion of the target group ARN\.
This is an example: app/EC2Co\-EcsEl\-1TKLTMITMM0EO/f37c06a68c1748aa/targetgroup/EC2Co\-Defau\-LDNM7Q3ZH1ZN/6d4ea56ca2d6a18d\.  
To find the ARN for an Application Load Balancer, use the [DescribeLoadBalancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_DescribeLoadBalancers.html) API operation\. To find the ARN for the target group, use the [DescribeTargetGroups](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_DescribeTargetGroups.html) API operation\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1023`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-autoscalingplans-scalingplan-predefinedscalingmetricspecification--seealso"></a>
+ [AWS Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/plans/userguide/what-is-aws-auto-scaling.html)