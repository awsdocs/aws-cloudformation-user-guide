# AWS::AutoScalingPlans::ScalingPlan PredefinedLoadMetricSpecification<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification"></a>

 `PredefinedLoadMetricSpecification` is a subproperty of [ScalingInstruction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscalingplans-scalingplan-scalinginstruction.html) that specifies a predefined load metric for predictive scaling to use with AWS Auto Scaling\.

After creating your scaling plan, you can use the AWS Auto Scaling console to visualize forecasts for the specified metric\. For more information, see [View Scaling Information for a Resource](https://docs.aws.amazon.com/autoscaling/plans/userguide/gs-create-scaling-plan.html#gs-view-resource) in the *AWS Auto Scaling User Guide*\.



## Syntax<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-syntax.json"></a>

```
{
  "[PredefinedLoadMetricType](#cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-predefinedloadmetrictype)" : String,
  "[ResourceLabel](#cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-syntax.yaml"></a>

```
  [PredefinedLoadMetricType](#cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-predefinedloadmetrictype): String
  [ResourceLabel](#cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification-properties"></a>

`PredefinedLoadMetricType`  <a name="cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-predefinedloadmetrictype"></a>
The metric type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALBTargetGroupRequestCount | ASGTotalCPUUtilization | ASGTotalNetworkIn | ASGTotalNetworkOut`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLabel`  <a name="cfn-autoscalingplans-scalingplan-predefinedloadmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\. You can't specify a resource label unless the metric type is `ALBTargetGroupRequestCount` and there is a target group for an Application Load Balancer attached to the Auto Scaling group\.  
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

## See also<a name="aws-properties-autoscalingplans-scalingplan-predefinedloadmetricspecification--seealso"></a>
+ [AWS Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/plans/userguide/what-is-aws-auto-scaling.html)