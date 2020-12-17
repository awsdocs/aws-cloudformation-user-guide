# AWS::ApplicationAutoScaling::ScalingPolicy<a name="aws-resource-applicationautoscaling-scalingpolicy"></a>

The `AWS::ApplicationAutoScaling::ScalingPolicy` resource defines a scaling policy that Application Auto Scaling uses to adjust your application resources\. 

For more information about Application Auto Scaling scaling policies, see the [Application Auto Scaling User Guide](https://docs.aws.amazon.com/autoscaling/application/userguide/what-is-application-auto-scaling.html)\.

## Syntax<a name="aws-resource-applicationautoscaling-scalingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
  "Properties" : {
      "[PolicyName](#cfn-applicationautoscaling-scalingpolicy-policyname)" : String,
      "[PolicyType](#cfn-applicationautoscaling-scalingpolicy-policytype)" : String,
      "[ResourceId](#cfn-applicationautoscaling-scalingpolicy-resourceid)" : String,
      "[ScalableDimension](#cfn-applicationautoscaling-scalingpolicy-scalabledimension)" : String,
      "[ScalingTargetId](#cfn-applicationautoscaling-scalingpolicy-scalingtargetid)" : String,
      "[ServiceNamespace](#cfn-applicationautoscaling-scalingpolicy-servicenamespace)" : String,
      "[StepScalingPolicyConfiguration](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration)" : StepScalingPolicyConfiguration,
      "[TargetTrackingScalingPolicyConfiguration](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration)" : TargetTrackingScalingPolicyConfiguration
    }
}
```

### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy-syntax.yaml"></a>

```
Type: AWS::ApplicationAutoScaling::ScalingPolicy
Properties: 
  [PolicyName](#cfn-applicationautoscaling-scalingpolicy-policyname): String
  [PolicyType](#cfn-applicationautoscaling-scalingpolicy-policytype): String
  [ResourceId](#cfn-applicationautoscaling-scalingpolicy-resourceid): String
  [ScalableDimension](#cfn-applicationautoscaling-scalingpolicy-scalabledimension): String
  [ScalingTargetId](#cfn-applicationautoscaling-scalingpolicy-scalingtargetid): String
  [ServiceNamespace](#cfn-applicationautoscaling-scalingpolicy-servicenamespace): String
  [StepScalingPolicyConfiguration](#cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration): 
    StepScalingPolicyConfiguration
  [TargetTrackingScalingPolicyConfiguration](#cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration): 
    TargetTrackingScalingPolicyConfiguration
```

## Properties<a name="aws-resource-applicationautoscaling-scalingpolicy-properties"></a>

`PolicyName`  <a name="cfn-applicationautoscaling-scalingpolicy-policyname"></a>
The name of the scaling policy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `\p{Print}+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyType`  <a name="cfn-applicationautoscaling-scalingpolicy-policytype"></a>
The Application Auto Scaling policy type\.   
The following policy types are supported:   
`TargetTrackingScaling`—Not supported for Amazon EMR  
`StepScaling`—Not supported for DynamoDB, Amazon Comprehend, Lambda, or Amazon Keyspaces \(for Apache Cassandra\)  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-applicationautoscaling-scalingpolicy-resourceid"></a>
The identifier of the resource associated with the scaling policy\. This string consists of the resource type and unique identifier\.  
+ ECS service \- The resource type is `service` and the unique identifier is the cluster name and service name\. Example: `service/default/sample-webapp`\.
+ Spot Fleet request \- The resource type is `spot-fleet-request` and the unique identifier is the Spot Fleet request ID\. Example: `spot-fleet-request/sfr-73fbd2ce-aa30-494c-8788-1cee4EXAMPLE`\.
+ EMR cluster \- The resource type is `instancegroup` and the unique identifier is the cluster ID and instance group ID\. Example: `instancegroup/j-2EEZNYKUA1NTV/ig-1791Y4E1L8YI0`\.
+ AppStream 2\.0 fleet \- The resource type is `fleet` and the unique identifier is the fleet name\. Example: `fleet/sample-fleet`\.
+ DynamoDB table \- The resource type is `table` and the unique identifier is the table name\. Example: `table/my-table`\.
+ DynamoDB global secondary index \- The resource type is `index` and the unique identifier is the index name\. Example: `table/my-table/index/my-table-index`\.
+ Aurora DB cluster \- The resource type is `cluster` and the unique identifier is the cluster name\. Example: `cluster:my-db-cluster`\.
+ Amazon SageMaker endpoint variant \- The resource type is `variant` and the unique identifier is the resource ID\. Example: `endpoint/my-end-point/variant/KMeansClustering`\.
+ Custom resources are not supported with a resource type\. This parameter must specify the `OutputValue` from the CloudFormation template stack used to access the resources\. The unique identifier is defined by the service provider\. More information is available in our [GitHub repository](https://github.com/aws/aws-auto-scaling-custom-resource)\.
+ Amazon Comprehend document classification endpoint \- The resource type and unique identifier are specified using the endpoint ARN\. Example: `arn:aws:comprehend:us-west-2:123456789012:document-classifier-endpoint/EXAMPLE`\.
+ Amazon Comprehend entity recognizer endpoint \- The resource type and unique identifier are specified using the endpoint ARN\. Example: `arn:aws:comprehend:us-west-2:123456789012:entity-recognizer-endpoint/EXAMPLE`\.
+ Lambda provisioned concurrency \- The resource type is `function` and the unique identifier is the function name with a function version or alias name suffix that is not `$LATEST`\. Example: `function:my-function:prod` or `function:my-function:1`\.
+ Amazon Keyspaces table \- The resource type is `table` and the unique identifier is the table name\. Example: `keyspace/mykeyspace/table/mytable`\.
+ Amazon MSK cluster \- The resource type and unique identifier are specified using the cluster ARN\. Example: `arn:aws:kafka:us-east-1:123456789012:cluster/demo-cluster-1/6357e0b2-0e6a-4b86-a0b4-70df934c2e31-5`\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScalableDimension`  <a name="cfn-applicationautoscaling-scalingpolicy-scalabledimension"></a>
The scalable dimension\. This string consists of the service namespace, resource type, and scaling property\.  
+  `ecs:service:DesiredCount` \- The desired task count of an ECS service\.
+  `ec2:spot-fleet-request:TargetCapacity` \- The target capacity of a Spot Fleet request\.
+  `elasticmapreduce:instancegroup:InstanceCount` \- The instance count of an EMR Instance Group\.
+  `appstream:fleet:DesiredCapacity` \- The desired capacity of an AppStream 2\.0 fleet\.
+  `dynamodb:table:ReadCapacityUnits` \- The provisioned read capacity for a DynamoDB table\.
+  `dynamodb:table:WriteCapacityUnits` \- The provisioned write capacity for a DynamoDB table\.
+  `dynamodb:index:ReadCapacityUnits` \- The provisioned read capacity for a DynamoDB global secondary index\.
+  `dynamodb:index:WriteCapacityUnits` \- The provisioned write capacity for a DynamoDB global secondary index\.
+  `rds:cluster:ReadReplicaCount` \- The count of Aurora Replicas in an Aurora DB cluster\. Available for Aurora MySQL\-compatible edition and Aurora PostgreSQL\-compatible edition\.
+  `sagemaker:variant:DesiredInstanceCount` \- The number of EC2 instances for an Amazon SageMaker model endpoint variant\.
+  `custom-resource:ResourceType:Property` \- The scalable dimension for a custom resource provided by your own application or service\.
+  `comprehend:document-classifier-endpoint:DesiredInferenceUnits` \- The number of inference units for an Amazon Comprehend document classification endpoint\.
+  `comprehend:entity-recognizer-endpoint:DesiredInferenceUnits` \- The number of inference units for an Amazon Comprehend entity recognizer endpoint\.
+  `lambda:function:ProvisionedConcurrency` \- The provisioned concurrency for a Lambda function\.
+  `cassandra:table:ReadCapacityUnits` \- The provisioned read capacity for an Amazon Keyspaces table\.
+  `cassandra:table:WriteCapacityUnits` \- The provisioned write capacity for an Amazon Keyspaces table\.
+  `kafka:broker-storage:VolumeSize` \- The provisioned volume size \(in GiB\) for brokers in an Amazon MSK cluster\.
*Required*: No  
*Type*: String  
*Allowed values*: `appstream:fleet:DesiredCapacity | cassandra:table:ReadCapacityUnits | cassandra:table:WriteCapacityUnits | comprehend:document-classifier-endpoint:DesiredInferenceUnits | comprehend:entity-recognizer-endpoint:DesiredInferenceUnits | custom-resource:ResourceType:Property | dynamodb:index:ReadCapacityUnits | dynamodb:index:WriteCapacityUnits | dynamodb:table:ReadCapacityUnits | dynamodb:table:WriteCapacityUnits | ec2:spot-fleet-request:TargetCapacity | ecs:service:DesiredCount | elasticmapreduce:instancegroup:InstanceCount | kafka:broker-storage:VolumeSize | lambda:function:ProvisionedConcurrency | rds:cluster:ReadReplicaCount | sagemaker:variant:DesiredInstanceCount`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ScalingTargetId`  <a name="cfn-applicationautoscaling-scalingpolicy-scalingtargetid"></a>
The AWS CloudFormation\-generated ID of an Application Auto Scaling scalable target\. For more information about the ID, see the Return Value section of the `AWS::ApplicationAutoScaling::ScalableTarget` resource\.  
You must specify either the `ScalingTargetId` property, or the `ResourceId`, `ScalableDimension`, and `ServiceNamespace` properties, but not both\. 
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceNamespace`  <a name="cfn-applicationautoscaling-scalingpolicy-servicenamespace"></a>
The namespace of the AWS service that provides the resource, or a `custom-resource`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `appstream | cassandra | comprehend | custom-resource | dynamodb | ec2 | ecs | elasticmapreduce | kafka | lambda | rds | sagemaker`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StepScalingPolicyConfiguration`  <a name="cfn-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration"></a>
A step scaling policy\.  
*Required*: No  
*Type*: [StepScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-stepscalingpolicyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTrackingScalingPolicyConfiguration`  <a name="cfn-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration"></a>
A target tracking scaling policy\.  
*Required*: No  
*Type*: [TargetTrackingScalingPolicyConfiguration](aws-properties-applicationautoscaling-scalingpolicy-targettrackingscalingpolicyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-applicationautoscaling-scalingpolicy-return-values"></a>

### Ref<a name="aws-resource-applicationautoscaling-scalingpolicy-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the Application Auto Scaling scaling policy Amazon Resource Name \(ARN\)\. For example: `arn:aws:autoscaling:us-east-2:123456789012:scalingPolicy:12ab3c4d-56789-0ef1-2345-6ghi7jk8lm90:resource/ecs/service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH:policyName/MyStepPolicy`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-applicationautoscaling-scalingpolicy--examples"></a>

The following examples create scaling policies for a scalable target that is registered with Application Auto Scaling\. 

For more template snippets, see [Application Auto Scaling template examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html#scenario-app-as-template-examples)\.

### Target tracking scaling policy with a predefined metric<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_tracking_scaling_policy_with_a_predefined_metric"></a>

This example shows how to declare a new AWS::ApplicationAutoScaling::ScalingPolicy resource to create a new scaling policy using the `TargetTrackingScaling` policy type\.

In this snippet, the policy specifies the `ECSServiceAverageCPUUtilization` predefined metric\. The metrics used with a target tracking scaling policy are either custom or predefined\. For the list of predefined metrics, see [PredefinedMetricSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalingpolicy-predefinedmetricspecification.html)\. When the metric is at or exceeds 75 percent, the scaling policy increases \(scales out\) the capacity of the scalable target, and when it falls below 75 percent, the scaling policy decreases \(scales in\) the capacity of the scalable target\. The scaling policy has a 60 second cooldown period after every scaling activity\.

#### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_tracking_scaling_policy_with_a_predefined_metric--json"></a>

```
{
  "Resources":{
    "TargetTrackingScalingPolicy":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":"cpu75-target-tracking-scaling-policy",
        "PolicyType":"TargetTrackingScaling",
        "ScalingTargetId":{
          "Ref":"ScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":75.0,
          "ScaleInCooldown":60,
          "ScaleOutCooldown":60,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ECSServiceAverageCPUUtilization"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Target_tracking_scaling_policy_with_a_predefined_metric--yaml"></a>

```
---
Resources:
  TargetTrackingScalingPolicy:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: cpu75-target-tracking-scaling-policy
      PolicyType: TargetTrackingScaling
      ScalingTargetId: !Ref ScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 75.0
        ScaleInCooldown: 60
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: ECSServiceAverageCPUUtilization
```

### Step scaling policy<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_scaling_policy"></a>

The following example creates a scaling policy with the `StepScaling` policy type and the `ChangeInCapacity` adjustment type\. When an associated alarm is triggered, the policy increases the capacity of the scalable target based on the following step adjustments \(assuming a CloudWatch alarm threshold of 70 percent\): 
+ Increase capacity by 1 when the value of the metric is greater than or equal to 70 percent but less than 85 percent 
+ Increase capacity by 2 when the value of the metric is greater than or equal to 85 percent but less than 95 percent 
+ Increase capacity by 3 when the value of the metric is greater than or equal to 95 percent 

In this snippet, the scaling policy has a 600 second cooldown period after every scaling activity\.

#### JSON<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_scaling_policy--json"></a>

```
{
  "Resources":{
    "PolicyHigh":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":"PolicyHigh",
        "PolicyType":"StepScaling",
        "ScalingTargetId":{
          "Ref":"ScalableTarget"
        },
        "StepScalingPolicyConfiguration":{
          "AdjustmentType":"ChangeInCapacity",
          "Cooldown":600,
          "MetricAggregationType":"Average",
          "StepAdjustments":[
            {
              "MetricIntervalLowerBound":0,
              "MetricIntervalUpperBound":15,
              "ScalingAdjustment":1
            },
            {
              "MetricIntervalLowerBound":15,
              "MetricIntervalUpperBound":25,
              "ScalingAdjustment":2
            },
            {
              "MetricIntervalLowerBound":25,
              "ScalingAdjustment":3
            }
          ]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-applicationautoscaling-scalingpolicy--examples--Step_scaling_policy--yaml"></a>

```
---
Resources:
  PolicyHigh:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: PolicyHigh
      PolicyType: StepScaling
      ScalingTargetId:
        Ref: ScalableTarget
      StepScalingPolicyConfiguration:
        AdjustmentType: ChangeInCapacity
        Cooldown: 600
        MetricAggregationType: Average
        StepAdjustments:
        - MetricIntervalLowerBound: 0
          MetricIntervalUpperBound: 15
          ScalingAdjustment: 1
        - MetricIntervalLowerBound: 15
          MetricIntervalUpperBound: 25
          ScalingAdjustment: 2
        - MetricIntervalLowerBound: 25
          ScalingAdjustment: 3
```

## See also<a name="aws-resource-applicationautoscaling-scalingpolicy--seealso"></a>
+ [PutScalingPolicy](https://docs.aws.amazon.com/autoscaling/application/APIReference/API_PutScalingPolicy.html) in the *Application Auto Scaling API Reference*
+ [Target tracking scaling policies](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html) in the *Application Auto Scaling User Guide*
+ [Step scaling policies](https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-step-scaling-policies.html) in the *Application Auto Scaling User Guide*
+ [How to use AWS CloudFormation to configure auto scaling for Amazon DynamoDB tables and indexes](http://aws.amazon.com/blogs/database/how-to-use-aws-cloudformation-to-configure-auto-scaling-for-amazon-dynamodb-tables-and-indexes/)

