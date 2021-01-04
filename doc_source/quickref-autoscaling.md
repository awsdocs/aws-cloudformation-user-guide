# Auto scaling template snippets<a name="quickref-autoscaling"></a>

The following examples show different snippets to include in templates for use with Amazon EC2 Auto Scaling or Application Auto Scaling\. 

Amazon EC2 Auto Scaling enables you to automatically scale Amazon EC2 instances, either with scaling policies or with scheduled scaling\. Auto Scaling groups are collections of Amazon EC2 instances that enable automatic scaling and fleet management features, such as health checks and integration with Elastic Load Balancing\.

Application Auto Scaling provides automatic scaling of different resources beyond Amazon EC2, either with scaling policies or with scheduled scaling\. 

**Topics**
+ [Declaring a launch configuration](#scenario-as-launch-config)
+ [Declaring a single instance Auto Scaling group](#scenario-single-instance-as-group)
+ [Declaring an Auto Scaling group with load balancing](#scenario-as-group)
+ [Declaring a scaling policy with a CloudWatch alarm](#scenario-as-policy)
+ [Declaring an Auto Scaling group with a launch template and notifications](#scenario-as-notification)
+ [Declaring an Auto Scaling group with an UpdatePolicy](#scenario-as-updatepolicy)
+ [Application Auto Scaling template examples](#scenario-app-as-template-examples)

## Declaring a launch configuration<a name="scenario-as-launch-config"></a>

This example shows an [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) resource for an Auto Scaling group where you specify values for the `ImageId`, `InstanceType`, and `SecurityGroups` properties\. The `SecurityGroups` property specifies both the logical name of an [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resource that is specified in the template, and an existing EC2 security group named `myExistingEC2SecurityGroup`\.

### JSON<a name="quickref-autoscaling-example-1.json"></a>

```
1. "mySimpleConfig" : {
2.    "Type" : "AWS::AutoScaling::LaunchConfiguration",
3.    "Properties" : {
4.       "ImageId" : "ami-02354e95b39ca8dec",
5.       "SecurityGroups" : [ { "Ref" : "logicalName" }, "myExistingEC2SecurityGroup" ],
6.       "InstanceType" : "t3.micro"
7.    }
8. }
```

### YAML<a name="quickref-autoscaling-example-1.yaml"></a>

```
1. mySimpleConfig:
2.   Type: AWS::AutoScaling::LaunchConfiguration
3.   Properties:
4.     ImageId: ami-02354e95b39ca8dec
5.     SecurityGroups:
6.     - Ref: logicalName
7.     - myExistingEC2SecurityGroup
8.     InstanceType: t3.micro
```

## Declaring a single instance Auto Scaling group<a name="scenario-single-instance-as-group"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource with a single instance to help you get started\. The `VPCZoneIdentifier` property of the Auto Scaling group specifies a list of existing subnets in different Availability Zones\. You must specify the applicable subnet IDs from your account before you create your stack\. The `LaunchConfigurationName` property references an [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) resource with the logical name `mySimpleConfig` that is defined in your template\.

### JSON<a name="quickref-autoscaling-example-2.json"></a>

```
 1. "myASG" : {
 2.    "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.    "Properties" : {
 4.       "VPCZoneIdentifier" : [ "subnetIdAz1", "subnetIdAz2", "subnetIdAz3" ],
 5.       "LaunchConfigurationName" : { "Ref" : "mySimpleConfig" },
 6.       "MinSize" : "0",
 7.       "MaxSize" : "1",
 8.       "DesiredCapacity" : "1"
 9.    }
10. }
```

### YAML<a name="quickref-autoscaling-example-2.yaml"></a>

```
 1. myASG:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   Properties:
 4.     VPCZoneIdentifier:
 5.       - subnetIdAz1
 6.       - subnetIdAz2
 7.       - subnetIdAz3
 8.     LaunchConfigurationName: !Ref mySimpleConfig
 9.     MinSize: '0'
10.     MaxSize: '1'
11.     DesiredCapacity: '1'
```

## Declaring an Auto Scaling group with load balancing<a name="scenario-as-group"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource for load balancing over multiple servers\. It specifies the logical names of AWS resources declared elsewhere in the same template\. 

1. The `VPCZoneIdentifier` property specifies the logical names of two [AWS::EC2::Subnet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html) resources where the Auto Scaling group's EC2 instances will be created: `myPublicSubnet1` and `myPublicSubnet2`\. 

1.  The `LaunchConfigurationName` property specifies an [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) resource with the logical name `mySimpleConfig`\.

1. The `TargetGroupARNs` property lists the target groups for an Application Load Balancer or Network Load Balancer used to route traffic to the Auto Scaling group\. In this example, one target group is specified, an [AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html) resource with the logical name `myTargetGroup`\.

### JSON<a name="quickref-autoscaling-example-2.json"></a>

```
 1. "myServerGroup" : {
 2.    "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.    "Properties" : {
 4.       "VPCZoneIdentifier" : [ { "Ref" : "myPublicSubnet1" }, { "Ref" : "myPublicSubnet2" } ],
 5.       "LaunchConfigurationName" : { "Ref" : "mySimpleConfig" },
 6.       "MinSize" : "1",
 7.       "MaxSize" : "5",
 8.       "HealthCheckGracePeriod" : 300,
 9.       "MaxInstanceLifetime" : 2592000,
10.       "TargetGroupARNs" : [ { "Ref" : "myTargetGroup" } ]
11.    }
12. }
```

### YAML<a name="quickref-autoscaling-example-2.yaml"></a>

```
 1. myServerGroup:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   Properties:
 4.     VPCZoneIdentifier:
 5.       - !Ref myPublicSubnet1
 6.       - !Ref myPublicSubnet2
 7.     LaunchConfigurationName: !Ref mySimpleConfig
 8.     MinSize: '1'
 9.     MaxSize: '5'
10.     HealthCheckGracePeriod: 300
11.     MaxInstanceLifetime: 2592000
12.     TargetGroupARNs:
13.       - !Ref myTargetGroup
```

### See also<a name="scenario-as-group-see-also"></a>

For a detailed example that creates an Auto Scaling group with a target tracking scaling policy based on the `ALBRequestCountPerTarget` predefined metric for your Application Load Balancer, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html#aws-properties-as-policy--examples) section in the AWS::AutoScaling::ScalingPolicy resource\.

## Declaring a scaling policy with a CloudWatch alarm<a name="scenario-as-policy"></a>

This example shows an [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html) resource that scales out the Auto Scaling group using a simple scaling policy\. The `AdjustmentType` property specifies `ChangeInCapacity`, which means that the `ScalingAdjustment` represents the number of instances to add \(if `ScalingAdjustment` is positive\) or delete \(if it is negative\)\. In this example, `ScalingAdjustment` is 1; therefore, the policy increments the number of EC2 instances in the group by 1 when the alarm threshold is breached\.

The [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html) resource `CPUAlarmHigh` specifies the scaling policy `myScaleOutPolicy` as the action to run when the alarm is in an ALARM state \(`AlarmActions`\)\.

### JSON<a name="quickref-autoscaling-example-3.json"></a>

```
 1. "myScaleOutPolicy" : {
 2.    "Type" : "AWS::AutoScaling::ScalingPolicy",
 3.    "Properties" : {
 4.       "AdjustmentType" : "ChangeInCapacity",
 5.       "AutoScalingGroupName" : { "Ref" : "logicalName" },
 6.       "ScalingAdjustment" : "1"
 7.    }
 8. },
 9. "CPUAlarmHigh" : {
10.    "Type" : "AWS::CloudWatch::Alarm",
11.    "Properties" : {
12.       "EvaluationPeriods" : "1",
13.       "Statistic" : "Average",
14.       "Threshold" : "10",
15.       "AlarmDescription" : "Alarm if CPU too high or metric disappears indicating instance is down",
16.       "Period" : "60",
17.       "AlarmActions" : [ { "Ref" : "myScaleOutPolicy" } ],
18.       "Namespace" : "AWS/EC2",
19.       "Dimensions" : [ {
20.          "Name" : "AutoScalingGroupName",
21.          "Value" : { "Ref" : "logicalName" }
22.       } ],
23.       "ComparisonOperator" : "GreaterThanThreshold",
24.       "MetricName" : "CPUUtilization"
25.    }
26. }
```

### YAML<a name="quickref-autoscaling-example-3.yaml"></a>

```
 1. myScaleOutPolicy:
 2.   Type: AWS::AutoScaling::ScalingPolicy
 3.   Properties:
 4.     AdjustmentType: ChangeInCapacity
 5.     AutoScalingGroupName: !Ref logicalName
 6.     ScalingAdjustment: '1'
 7. CPUAlarmHigh:
 8.   Type: AWS::CloudWatch::Alarm
 9.   Properties:
10.     EvaluationPeriods: '1'
11.     Statistic: Average
12.     Threshold: '10'
13.     AlarmDescription: Alarm if CPU too high or metric disappears indicating instance
14.       is down
15.     Period: '60'
16.     AlarmActions:
17.     - !Ref myScaleOutPolicy
18.     Namespace: AWS/EC2
19.     Dimensions:
20.     - Name: AutoScalingGroupName
21.       Value:
22.         Ref: logicalName
23.     ComparisonOperator: GreaterThanThreshold
24.     MetricName: CPUUtilization
```

### See also<a name="scenario-as-policy-see-also"></a>

For example templates for the `TargetTrackingScaling` and `StepScaling` policy types, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html#aws-properties-as-policy--examples) section in the AWS::AutoScaling::ScalingPolicy resource\.

## Declaring an Auto Scaling group with a launch template and notifications<a name="scenario-as-notification"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource that sends Amazon SNS notifications when the specified events take place\. The `NotificationConfigurations` property specifies the SNS topic where AWS CloudFormation sends a notification and the events that will cause AWS CloudFormation to send notifications\. When the events specified by `NotificationTypes` occur, AWS CloudFormation will send a notification to the SNS topic specified by `TopicARN`\. When you launch the stack, AWS CloudFormation creates an [AWS::SNS::Subscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sns-subscription.html) resource \(`snsTopicForAutoScalingGroup`\) that's declared within the same template\.

The `AvailabilityZones` and `VPCZoneIdentifier` properties of the Auto Scaling group reference parameter values that you pass to the template when creating or updating a stack\. The `LaunchTemplate` property references the logical name of an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource declared elsewhere in the same template\.

### JSON<a name="quickref-autoscaling-example-4.json"></a>

```
 1. "myASG" : {
 2.   "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.   "DependsOn": [
 4.     "snsTopicForAutoScalingGroup"
 5.   ],
 6.   "Properties" : {
 7.     "AvailabilityZones" : { "Ref" : "AZs" },
 8.     "VPCZoneIdentifier" : { "Ref" : "Subnets" },
 9.     "LaunchTemplate" : {
10.       "LaunchTemplateId" : {
11.         "Ref" : "logicalName"
12.       },
13.       "Version" : {
14.         "Fn::GetAtt" : [
15.           "logicalName",
16.           "LatestVersionNumber"
17.         ]
18.       }
19.     },
20.     "MinSize" : "1",
21.     "MaxSize" : "5",
22.     "NotificationConfigurations" : [
23.       {
24.         "TopicARN" : { "Ref" : "snsTopicForAutoScalingGroup" },
25.         "NotificationTypes" : [
26.           "autoscaling:EC2_INSTANCE_LAUNCH",
27.           "autoscaling:EC2_INSTANCE_LAUNCH_ERROR",
28.           "autoscaling:EC2_INSTANCE_TERMINATE",
29.           "autoscaling:EC2_INSTANCE_TERMINATE_ERROR",
30.           "autoscaling:TEST_NOTIFICATION"
31.         ]
32.       }
33.     ]
34.   }
35. }
```

### YAML<a name="quickref-autoscaling-example-4.yaml"></a>

```
 1. myASG:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   DependsOn:
 4.     - snsTopicForAutoScalingGroup
 5.   Properties:
 6.     AvailabilityZones: !Ref AZs
 7.     VPCZoneIdentifier: !Ref Subnets
 8.     LaunchTemplate:
 9.       LaunchTemplateId: !Ref logicalName
10.       Version: !GetAtt logicalName.LatestVersionNumber
11.     MinSize: '1'
12.     MaxSize: '5'
13.     NotificationConfigurations:
14.     - TopicARN: !Ref snsTopicForAutoScalingGroup
15.       NotificationTypes:
16.       - autoscaling:EC2_INSTANCE_LAUNCH
17.       - autoscaling:EC2_INSTANCE_LAUNCH_ERROR
18.       - autoscaling:EC2_INSTANCE_TERMINATE
19.       - autoscaling:EC2_INSTANCE_TERMINATE_ERROR
20.       - autoscaling:TEST_NOTIFICATION
```

### See also<a name="scenario-as-notification-see-also"></a>

For more examples that specify a launch template for an Auto Scaling group, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#aws-properties-as-group--examples) section in the AWS::AutoScaling::AutoScalingGroup resource\.

## Declaring an Auto Scaling group with an UpdatePolicy<a name="scenario-as-updatepolicy"></a>

The following example specifies an [UpdatePolicy attribute](aws-attribute-updatepolicy.md) for an Auto Scaling group\. The sample update policy instructs CloudFormation to perform a rolling update using the `AutoScalingRollingUpdate` property\. The rolling update makes changes to the Auto Scaling group in small batches \(for this example, instance by instance\) based on the `MaxBatchSize` and a pause time between batches of updates based on the `PauseTime`\. The `MinInstancesInService` attribute specifies the minimum number of instances that must be in service within the Auto Scaling group while CloudFormation updates old instances\. 

The `WaitOnResourceSignals` attribute is set to `true`\. CloudFormation must receive a signal from each new instance within the specified `PauseTime` before continuing the update\. To signal the Auto Scaling group, a [cfn\-signal](cfn-signal.md) helper script \(not shown\) is run on each instance\. While the stack update is in progress, the following EC2 Auto Scaling processes are suspended: `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, and `ScheduledActions`\. Note: Do not suspend the `Launch`, `Terminate`, or `AddToLoadBalancer` \(if the Auto Scaling group is being used with Elastic Load Balancing\) process types because doing so can prevent the rolling update from functioning properly\. 

### JSON<a name="quickref-autoscaling-example-5.json"></a>

```
"myASG" : {
   "UpdatePolicy" : {
      "AutoScalingRollingUpdate" : {
         "MinInstancesInService" : "1",
         "MaxBatchSize" : "1",
         "PauseTime" : "PT12M5S",
         "WaitOnResourceSignals" : "true",
         "SuspendProcesses" : [
            "HealthCheck",
            "ReplaceUnhealthy",
            "AZRebalance",
            "AlarmNotification",
            "ScheduledActions"
         ]
      }
   },
   "Type" : "AWS::AutoScaling::AutoScalingGroup",
   "Properties" : {
      "AvailabilityZones" : { "Ref" : "AZs" },
      "VPCZoneIdentifier" : { "Ref" : "Subnets" },
      "LaunchConfigurationName" : { "Ref" : "logicalName" },
      "MaxSize" : "5",
      "MinSize" : "1"
   }
}
```

### YAML<a name="quickref-autoscaling-example-5.yaml"></a>

```
myASG:
  UpdatePolicy:
    AutoScalingRollingUpdate:
      MinInstancesInService: '1'
      MaxBatchSize: '1'
      PauseTime: PT12M5S
      WaitOnResourceSignals: true
      SuspendProcesses:
        - HealthCheck
        - ReplaceUnhealthy
        - AZRebalance
        - AlarmNotification
        - ScheduledActions
  Type: AWS::AutoScaling::AutoScalingGroup
  Properties:
    AvailabilityZones: !Ref AZs
    VPCZoneIdentifier: !Ref Subnets
    LaunchConfigurationName: !Ref logicalName
    MaxSize: '5'
    MinSize: '1'
```

## Application Auto Scaling template examples<a name="scenario-app-as-template-examples"></a>

This section provides AWS CloudFormation template examples for Application Auto Scaling scaling policies and scheduled actions for different AWS resources\. 

**Topics**
+ [Declaring a scaling policy for an Aurora DB cluster](#w7739ab1c27c22c15c23c11)
+ [Declaring a scaling policy for a DynamoDB table](#w7739ab1c27c22c15c23c13)
+ [Declaring a scaling policy for an Amazon ECS service](#w7739ab1c27c22c15c23c15)
+ [Declaring a scheduled action for a Lambda function](#w7739ab1c27c22c15c23c17)
+ [Declaring a scheduled action for a Spot Fleet](#w7739ab1c27c22c15c23c19)

**Important**  
When an Application Auto Scaling snippet is included in the template, you should declare a dependency on the specific scalable resource that is created through the template using the [DependsOn](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) attribute\. This overrides the default parallelism and directs AWS CloudFormation to operate on resources in a specified order\. Otherwise, the scaling configuration might be applied before the resource has been set up completely\.

### Declaring a scaling policy for an Aurora DB cluster<a name="w7739ab1c27c22c15c23c11"></a>

In this snippet, you register an existing [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html) resource named `my-db-cluster`\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource indicates that the DB cluster should be dynamically scaled to have from one to eight Aurora Replicas\. You also apply a target tracking scaling policy to the cluster using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. 

In this configuration, the `RDSReaderAverageCPUUtilization` predefined metric is used to adjust an Aurora DB cluster based on an average CPU utilization of 40 percent across all Aurora Replicas in that Aurora DB cluster\. The configuration provides a scale\-in cooldown period of 10 minutes and a scale\-out cooldown period of 5 minutes\.

#### JSON<a name="quickref-autoscaling-example-7.json"></a>

```
{
  "Resources" : {
    "ScalableTarget" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties" : {
        "MaxCapacity" : 8,
        "MinCapacity" : 1,
        "RoleARN" : { "Fn::Sub" : "arn:aws:iam::${AWS::AccountId}:role/aws-service-role/rds.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_RDSCluster" },
        "ServiceNamespace" : "rds",
        "ScalableDimension" : "rds:cluster:ReadReplicaCount",
        "ResourceId" : "cluster:my-db-cluster"
      }
    },
    "ScalingPolicyDBCluster" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties" : {
        "PolicyName" : { "Fn::Sub" : "${AWS::StackName}-target-tracking-cpu40" },
        "PolicyType" : "TargetTrackingScaling",
        "ServiceNamespace" : "rds",
        "ScalableDimension" : "rds:cluster:ReadReplicaCount",
        "ResourceId" : "cluster:my-db-cluster",
        "TargetTrackingScalingPolicyConfiguration" : {
          "TargetValue" : 40,
          "PredefinedMetricSpecification" : {
            "PredefinedMetricType" : "RDSReaderAverageCPUUtilization"
          },
          "ScaleInCooldown" : 600,
          "ScaleOutCooldown" : 300
        }
      }
    }
  }
}
```

#### YAML<a name="quickref-autoscaling-example-7.yaml"></a>

```
---
Resources:
  ScalableTarget:
    Type: 'AWS::ApplicationAutoScaling::ScalableTarget'
    Properties:
      MaxCapacity: 8
      MinCapacity: 1
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/rds.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_RDSCluster'
      ServiceNamespace: rds
      ScalableDimension: 'rds:cluster:ReadReplicaCount'
      ResourceId: 'cluster:my-db-cluster'
  ScalingPolicyDBCluster:
    Type: 'AWS::ApplicationAutoScaling::ScalingPolicy'
    Properties:
      PolicyName: !Sub ${AWS::StackName}-target-tracking-cpu40
      PolicyType: TargetTrackingScaling
      ServiceNamespace: rds
      ScalableDimension: 'rds:cluster:ReadReplicaCount'
      ResourceId: 'cluster:my-db-cluster'
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 40
        PredefinedMetricSpecification:
          PredefinedMetricType: RDSReaderAverageCPUUtilization
        ScaleInCooldown: 600
        ScaleOutCooldown: 300
```

### Declaring a scaling policy for a DynamoDB table<a name="w7739ab1c27c22c15c23c13"></a>

This snippet shows how to create a policy with the `TargetTrackingScaling` policy type and apply it to an [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html) resource using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource declares a scalable target to which this policy is applied, with a minimum of five write capacity units and a maximum of 15\. The scaling policy scales the table's write capacity throughput to maintain the target utilization at 50 percent based on the `DynamoDBWriteCapacityUtilization` predefined metric\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property with the logical name of the AWS::DynamoDB::Table resource that is specified in the same template\.

**Note**  
For more information about how to create an AWS CloudFormation template for DynamoDB resources, see the blog post [How to use AWS CloudFormation to configure auto scaling for Amazon DynamoDB tables and indexes](http://aws.amazon.com/blogs/database/how-to-use-aws-cloudformation-to-configure-auto-scaling-for-amazon-dynamodb-tables-and-indexes/) on the AWS Database Blog\.

#### JSON<a name="quickref-autoscaling-example-8.json"></a>

```
{
  "Resources" : {
    "WriteCapacityScalableTarget" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties" : {
        "MaxCapacity" : 15,
        "MinCapacity" : 5,
        "RoleARN" : { "Fn::Sub" : "arn:aws:iam::${AWS::AccountId}:role/aws-service-role/dynamodb.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_DynamoDBTable" },
        "ServiceNamespace" : "dynamodb",
        "ScalableDimension" : "dynamodb:table:WriteCapacityUnits",
        "ResourceId" : {
          "Fn::Join" : [
            "/",
            [
              "table",
              {
                "Ref" : "logicalName"
              }
            ]
          ]
        }
      }
    },
    "WriteScalingPolicy" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties" : {
        "PolicyName" : "WriteScalingPolicy",
        "PolicyType" : "TargetTrackingScaling",
        "ScalingTargetId" : { "Ref" : "WriteCapacityScalableTarget" },
        "TargetTrackingScalingPolicyConfiguration" : {
          "TargetValue" : 50.0,
          "ScaleInCooldown" : 60,
          "ScaleOutCooldown" : 60,
          "PredefinedMetricSpecification" : {
            "PredefinedMetricType" : "DynamoDBWriteCapacityUtilization"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="quickref-autoscaling-example-8.yaml"></a>

```
---
Resources:
  WriteCapacityScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: 15
      MinCapacity: 5
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/dynamodb.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_DynamoDBTable'
      ServiceNamespace: dynamodb
      ScalableDimension: dynamodb:table:WriteCapacityUnits
      ResourceId: !Join
        - /
        - - table
          - !Ref logicalName
  WriteScalingPolicy:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: WriteScalingPolicy
      PolicyType: TargetTrackingScaling
      ScalingTargetId: !Ref WriteCapacityScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 50.0
        ScaleInCooldown: 60
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: DynamoDBWriteCapacityUtilization
```

### Declaring a scaling policy for an Amazon ECS service<a name="w7739ab1c27c22c15c23c15"></a>

This snippet shows how to create a policy and apply it to an [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html) resource using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource declares a scalable target to which this policy is applied\. Application Auto Scaling can scale the number of tasks at a minimum of 1 task and a maximum of 2\.

It creates two scaling policies with the `TargetTrackingScaling` policy type\. The policies are used to scale the ECS service based on the service's average CPU and memory usage\. It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property with the logical names of the AWS::ECS::Cluster \(`myContainerCluster`\) and AWS::ECS::Service \(`myService`\) resources that are specified in the same template\.

#### JSON<a name="quickref-autoscaling-example-9.json"></a>

```
{
  "Resources" : {
    "ECSScalableTarget" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties" : {
        "MaxCapacity" : "2",
        "MinCapacity" : "1",
        "RoleARN" : { "Fn::Sub" : "arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ecs.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_ECSService" },
        "ServiceNamespace" : "ecs",
        "ScalableDimension" : "ecs:service:DesiredCount",
        "ResourceId" : {
          "Fn::Join" : [
            "/",
            [
              "service",
              {
                "Ref" : "myContainerCluster"
              },
              {
                "Fn::GetAtt" : [
                  "myService",
                  "Name"
                ]
              }
            ]
          ]
        }
      }
    },
    "ServiceScalingPolicyCPU" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties" : {
        "PolicyName" : { "Fn::Sub" : "${AWS::StackName}-target-tracking-cpu70" },
        "PolicyType" : "TargetTrackingScaling",
        "ScalingTargetId" : { "Ref" : "ECSScalableTarget" },
        "TargetTrackingScalingPolicyConfiguration" : {
          "TargetValue" : 70.0,
          "ScaleInCooldown" : 180,
          "ScaleOutCooldown" : 60,
          "PredefinedMetricSpecification" : {
            "PredefinedMetricType" : "ECSServiceAverageCPUUtilization"
          }
        }
      }
    },
    "ServiceScalingPolicyMem" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties" : {
        "PolicyName" : { "Fn::Sub" : "${AWS::StackName}-target-tracking-mem90" },
        "PolicyType" : "TargetTrackingScaling",
        "ScalingTargetId" : { "Ref" : "ECSScalableTarget" },
        "TargetTrackingScalingPolicyConfiguration" : {
          "TargetValue" : 90.0,
          "ScaleInCooldown" : 180,
          "ScaleOutCooldown" : 60,
          "PredefinedMetricSpecification" : {
            "PredefinedMetricType" : "ECSServiceAverageMemoryUtilization"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="quickref-autoscaling-example-9.yaml"></a>

```
---
Resources:
  ECSScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: '2'
      MinCapacity: '1'  
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ecs.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_ECSService'
      ServiceNamespace: ecs
      ScalableDimension: 'ecs:service:DesiredCount'
      ResourceId: !Join 
        - /
        - - service
          - !Ref myContainerCluster
          - !GetAtt myService.Name
  ServiceScalingPolicyCPU:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: !Sub ${AWS::StackName}-target-tracking-cpu70
      PolicyType: TargetTrackingScaling
      ScalingTargetId: !Ref ECSScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 70.0
        ScaleInCooldown: 180
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: ECSServiceAverageCPUUtilization
  ServiceScalingPolicyMem:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: !Sub ${AWS::StackName}-target-tracking-mem90
      PolicyType: TargetTrackingScaling
      ScalingTargetId: !Ref ECSScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 90.0
        ScaleInCooldown: 180
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: ECSServiceAverageMemoryUtilization
```

The following example applies a target tracking scaling policy with the `ALBRequestCountPerTarget` predefined metric to an ECS service\. The policy is used to add capacity to the ECS service when the request count per target \(per minute\) exceeds the target value\. Because the value of `DisableScaleIn` is set to `true`, the target tracking policy won't remove capacity from the scalable target\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html) intrinsic functions to construct the `ResourceLabel` property with the logical names of the AWS::ElasticLoadBalancingV2::LoadBalancer \(`myLoadBalancer`\) and AWS::ElasticLoadBalancingV2::TargetGroup \(`myTargetGroup`\) resources that are specified in the same template\.

The `MaxCapacity` and `MinCapacity` properties of the scalable target and the `TargetValue` property of the scaling policy reference parameter values that you pass to the template when creating or updating a stack\. 

#### JSON<a name="quickref-autoscaling-example-10.json"></a>

```
{
  "Resources" : {
    "ECSScalableTarget" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties" : {
        "MaxCapacity" : { "Ref" : "MaxCount" },
        "MinCapacity" : { "Ref" : "MinCount" },
        "RoleARN" : { "Fn::Sub" : "arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ecs.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_ECSService" },
        "ServiceNamespace" : "ecs",
        "ScalableDimension" : "ecs:service:DesiredCount",
        "ResourceId" : {
          "Fn::Join" : [
            "/",
            [
              "service",
              {
                "Ref" : "myContainerCluster"
              },
              {
                "Fn::GetAtt" : [
                  "myService",
                  "Name"
                ]
              }
            ]
          ]
        }
      }
    },
    "ServiceScalingPolicyALB" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties" : {
        "PolicyName" : "alb-requests-per-target-per-minute",
        "PolicyType" : "TargetTrackingScaling",
        "ScalingTargetId" : { "Ref" : "ECSScalableTarget" },
        "TargetTrackingScalingPolicyConfiguration" : {
          "TargetValue" : { "Ref" : "ALBPolicyTargetValue" },
          "ScaleInCooldown" : 180,
          "ScaleOutCooldown" : 30,
          "DisableScaleIn" : true,
          "PredefinedMetricSpecification" : {
            "PredefinedMetricType" : "ALBRequestCountPerTarget",
            "ResourceLabel" : {
              "Fn::Join" : [
                "/",
                [
                  {
                    "Fn::GetAtt" : [
                      "myLoadBalancer",
                      "LoadBalancerFullName"
                    ]
                  },
                  {
                    "Fn::GetAtt" : [
                      "myTargetGroup",
                      "TargetGroupFullName"
                    ]
                  }
                ]
              ]
            }
          }
        }
      }
    }
  }
}
```

#### YAML<a name="quickref-autoscaling-example-10.yaml"></a>

```
---
Resources:
  ECSScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: !Ref MaxCount
      MinCapacity: !Ref MinCount  
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ecs.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_ECSService'
      ServiceNamespace: ecs
      ScalableDimension: 'ecs:service:DesiredCount'
      ResourceId: !Join 
        - /
        - - service
          - !Ref myContainerCluster
          - !GetAtt myService.Name
  ServiceScalingPolicyALB:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: alb-requests-per-target-per-minute
      PolicyType: TargetTrackingScaling
      ScalingTargetId: !Ref ECSScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: !Ref ALBPolicyTargetValue
        ScaleInCooldown: 180
        ScaleOutCooldown: 30
        DisableScaleIn: true
        PredefinedMetricSpecification:
          PredefinedMetricType: ALBRequestCountPerTarget
          ResourceLabel: !Join 
            - '/' 
            - - !GetAtt myLoadBalancer.LoadBalancerFullName
              - !GetAtt myTargetGroup.TargetGroupFullName
```

### Declaring a scheduled action for a Lambda function<a name="w7739ab1c27c22c15c23c17"></a>

This snippet registers the provisioned concurrency for a function alias \([AWS::Lambda::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-alias.html)\) named `BLUE` using the [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource\. It also creates a scheduled action with a recurring schedule using a cron expression\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions in the `RoleARN` property to specify the ARN of the service\-linked role\. It uses the [Fn::Sub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html) intrinsic function to construct the `ResourceId` property with the logical name of the AWS::Lambda::Function or AWS::Serverless::Function resource that is specified in the same template\.

Note: You can't allocate provisioned concurrency on an alias that points to the unpublished version \($LATEST\)\. 

**Note**  
For more information about how to create an AWS CloudFormation template for Lambda resources, see the blog post [Scheduling AWS Lambda Provisioned Concurrency for recurring peak usage](http://aws.amazon.com/blogs/compute/scheduling-aws-lambda-provisioned-concurrency-for-recurring-peak-usage/) on the AWS Compute Blog\.

#### JSON<a name="quickref-autoscaling-example-11.json"></a>

```
{
  "ScalableTarget" : {
    "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
    "Properties" : {
      "MaxCapacity" : 0,
      "MinCapacity" : 0,
      "RoleARN" : {
        "Fn::Join" : [
          ":",
          [
            "arn:aws:iam:",
            {
              "Ref" : "AWS::AccountId"
            },
            "role/aws-service-role/lambda.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_LambdaConcurrency"
          ]
        ]
      },
      "ServiceNamespace" : "lambda",
      "ScalableDimension" : "lambda:function:ProvisionedConcurrency",
      "ResourceId" : { "Fn::Sub" : "function:${logicalName}:BLUE" },
      "ScheduledActions" : [
        {
          "EndTime" : "2020-12-31T12:00:00.000Z",
          "ScalableTargetAction" : {
            "MaxCapacity" : "500",
            "MinCapacity" : "50"
          },
          "ScheduledActionName" : "First",
          "Schedule" : "cron(0 18 * * ? *)"
        }
      ]
    }
  }
}
```

#### YAML<a name="quickref-autoscaling-example-11.yaml"></a>

```
ScalableTarget:
  Type: AWS::ApplicationAutoScaling::ScalableTarget
  Properties:
    MaxCapacity: 0
    MinCapacity: 0
    RoleARN: !Join 
      - ':'
      - - 'arn:aws:iam:'
        - !Ref 'AWS::AccountId'
        - role/aws-service-role/lambda.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_LambdaConcurrency
    ServiceNamespace: lambda
    ScalableDimension: lambda:function:ProvisionedConcurrency
    ResourceId: !Sub function:${logicalName}:BLUE
    ScheduledActions:
      - EndTime: '2020-12-31T12:00:00.000Z'
        ScalableTargetAction:
          MaxCapacity: '500'
          MinCapacity: '50'
        ScheduledActionName: First
        Schedule: 'cron(0 18 * * ? *)'
```

### Declaring a scheduled action for a Spot Fleet<a name="w7739ab1c27c22c15c23c19"></a>

This snippet shows how to create a scheduled action and apply it to an [AWS::EC2::SpotFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-spotfleet.html) resource using the [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource\. It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property with the logical name of the AWS::EC2::SpotFleet resource that is specified in the same template\.

Note: The Spot Fleet request must have a request type of `maintain`\. Automatic scaling is not supported for one\-time requests or Spot blocks\.

#### JSON<a name="quickref-autoscaling-example-12.json"></a>

```
{
  "Resources" : {
    "SpotFleetScalableTarget" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties" : {
        "MaxCapacity" : 0,
        "MinCapacity" : 0,
        "RoleARN" : { "Fn::Sub" : "arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ec2.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_EC2SpotFleetRequest" },
        "ServiceNamespace" : "ec2",
        "ScalableDimension" : "ec2:spot-fleet-request:TargetCapacity",
        "ResourceId" : {
          "Fn::Join" : [
            "/",
            [
              "spot-fleet-request",
              {
                "Ref" : "logicalName"
              }
            ]
          ]
        },
        "ScheduledActions" : [
          {
            "EndTime" : "2020-12-31T12:00:00.000Z",
            "ScalableTargetAction" : {
              "MaxCapacity" : "20",
              "MinCapacity" : "5"
            },
            "ScheduledActionName" : "First",
            "Schedule" : "cron(0 18 * * ? *)"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="quickref-autoscaling-example-12.yaml"></a>

```
---
Resources:
  SpotFleetScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: 0
      MinCapacity: 0
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ec2.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_EC2SpotFleetRequest'
      ServiceNamespace: ec2
      ScalableDimension: 'ec2:spot-fleet-request:TargetCapacity'
      ResourceId: !Join 
        - /
        - - spot-fleet-request
          - !Ref logicalName
      ScheduledActions:
        - EndTime: '2020-12-31T12:00:00.000Z'
          ScalableTargetAction:
            MaxCapacity: '20'
            MinCapacity: '5'
          ScheduledActionName: First
          Schedule: 'cron(0 18 * * ? *)'
```