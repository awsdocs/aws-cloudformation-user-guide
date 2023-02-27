# AWS::ApplicationAutoScaling::ScalingPolicy PredefinedMetricSpecification<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification"></a>

Contains predefined metric specification information for a target tracking scaling policy for Application Auto Scaling\.

`PredefinedMetricSpecification` is a property of the [AWS::ApplicationAutoScaling::ScalingPolicy TargetTrackingScalingPolicyConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.html) property type\. 

## Syntax<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax.json"></a>

```
{
  "[PredefinedMetricType](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype)" : String,
  "[ResourceLabel](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel)" : String
}
```

### YAML<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-syntax.yaml"></a>

```
  [PredefinedMetricType](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype): String
  [ResourceLabel](#cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel): String
```

## Properties<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification-properties"></a>

`PredefinedMetricType`  <a name="cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-predefinedmetrictype"></a>
The metric type\. The `ALBRequestCountPerTarget` metric type applies only to Spot fleet requests and ECS services\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALBRequestCountPerTarget | AppStreamAverageCapacityUtilization | CassandraReadCapacityUtilization | CassandraWriteCapacityUtilization | ComprehendInferenceUtilization | DynamoDBReadCapacityUtilization | DynamoDBWriteCapacityUtilization | EC2SpotFleetRequestAverageCPUUtilization | EC2SpotFleetRequestAverageNetworkIn | EC2SpotFleetRequestAverageNetworkOut | ECSServiceAverageCPUUtilization | ECSServiceAverageMemoryUtilization | ElastiCacheDatabaseMemoryUsageCountedForEvictPercentage | ElastiCachePrimaryEngineCPUUtilization | ElastiCacheReplicaEngineCPUUtilization | KafkaBrokerStorageUtilization | LambdaProvisionedConcurrencyUtilization | NeptuneReaderAverageCPUUtilization | RDSReaderAverageCPUUtilization | RDSReaderAverageDatabaseConnections | SageMakerVariantInvocationsPerInstance`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLabel`  <a name="cfn-applicationautoscaling-scalingpolicy-predefinedmetricspecification-resourcelabel"></a>
Identifies the resource associated with the metric type\. You can't specify a resource label unless the metric type is `ALBRequestCountPerTarget` and there is a target group attached to the Spot Fleet or ECS service\.  
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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification--seealso"></a>
+ [Application Auto Scaling template examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html#scenario-app-as-template-examples)
+ [Getting started](https://docs.aws.amazon.com/autoscaling/application/userguide/getting-started.html) in the *Application Auto Scaling User Guide*

