# Auto scaling template snippets<a name="quickref-autoscaling"></a>

The following examples show different snippets to include in templates for use with Amazon EC2 Auto Scaling or Application Auto Scaling\. 

Amazon EC2 Auto Scaling enables you to automatically scale Amazon EC2 instances, either with scaling policies or with scheduled scaling\. Auto Scaling groups are collections of Amazon EC2 instances that enable automatic scaling and fleet management features, such as health checks and integration with Elastic Load Balancing\.

Application Auto Scaling provides automatic scaling of different resources beyond Amazon EC2, either with scaling policies or with scheduled scaling\. 

**Topics**
+ [Declaring a launch configuration](#scenario-as-launch-config)
+ [Declaring an Auto Scaling group](#scenario-as-group)
+ [Declaring a scaling policy with a CloudWatch alarm](#scenario-as-policy)
+ [Declaring an Auto Scaling group with notifications](#scenario-as-notification)
+ [Declaring an Auto Scaling group with an UpdatePolicy](#scenario-as-updatepolicy)
+ [Application Auto Scaling template examples](#scenario-app-as-template-examples)

## Declaring a launch configuration<a name="scenario-as-launch-config"></a>

This example shows an [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) resource for an Auto Scaling group\. The SecurityGroups property specifies both an [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resource named myEC2SecurityGroup and an existing EC2 security group named myExistingEC2SecurityGroup\. The BlockDeviceMappings property lists two devices: a 50 gigabyte EBS volume mapped to /dev/sdk and a virtual device ephemeral0 mapped to /dev/sdc\. 

### JSON<a name="quickref-autoscaling-example-1.json"></a>

```
 1. "SimpleConfig" : {
 2.    "Type" : "AWS::AutoScaling::LaunchConfiguration",
 3.    "Properties" : {
 4.       "ImageId" : "ami-0ff8a91507f77f867",
 5.       "SecurityGroups" : [ { "Ref" : "myEC2SecurityGroup" }, "myExistingEC2SecurityGroup" ],
 6.       "InstanceType" : "m1.small",
 7.       "BlockDeviceMappings" : [ {
 8.             "DeviceName" : "/dev/sdk",
 9.             "Ebs" : {"VolumeSize" : "50"}
10.          }, {
11.             "DeviceName" : "/dev/sdc",
12.             "VirtualName" : "ephemeral0"
13.       } ]
14.    }
15. }
```

### YAML<a name="quickref-autoscaling-example-1.yaml"></a>

```
 1. SimpleConfig:
 2.   Type: AWS::AutoScaling::LaunchConfiguration
 3.   Properties:
 4.     ImageId: ami-0ff8a91507f77f867
 5.     SecurityGroups:
 6.     - Ref: myEC2SecurityGroup
 7.     - myExistingEC2SecurityGroup
 8.     InstanceType: m1.small
 9.     BlockDeviceMappings:
10.     - DeviceName: "/dev/sdk"
11.       Ebs:
12.         VolumeSize: '50'
13.     - DeviceName: "/dev/sdc"
14.       VirtualName: ephemeral0
```

## Declaring an Auto Scaling group<a name="scenario-as-group"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource\. The AvailabilityZones property specifies the Availability Zones where the Auto Scaling group's EC2 instances will be created\. In this example, the [Fn::GetAZs](intrinsic-function-reference-getavailabilityzones.md) function call `{ "Fn::GetAZs" : "" }` specifies all Availability Zones for the region in which the stack is created\. The LoadBalancerNames property lists the LoadBalancers used to route traffic to the Auto Scaling group\. In this example, one LoadBalancer is specified, the [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html) resource LB\.

### JSON<a name="quickref-autoscaling-example-2.json"></a>

```
 1. "MyServerGroup" : {
 2.    "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.    "Properties" : {
 4.       "AvailabilityZones" : { "Fn::GetAZs" : ""},
 5.       "LaunchConfigurationName" : { "Ref" : "SimpleConfig" },
 6.       "MinSize" : "1",
 7.       "MaxSize" : "3",
 8.       "LoadBalancerNames" : [ { "Ref" : "LB" } ]
 9.    }
10. }
```

### YAML<a name="quickref-autoscaling-example-2.yaml"></a>

```
 1. MyServerGroup:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   Properties:
 4.     AvailabilityZones:
 5.       Fn::GetAZs: ''
 6.     LaunchConfigurationName:
 7.       Ref: SimpleConfig
 8.     MinSize: '1'
 9.     MaxSize: '3'
10.     LoadBalancerNames:
11.     - Ref: LB
```

## Declaring a scaling policy with a CloudWatch alarm<a name="scenario-as-policy"></a>

This example shows an [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html) resource that scales up the Auto Scaling group asGroup using a simple scaling policy\. The `AdjustmentType` property specifies ChangeInCapacity, which means that the `ScalingAdjustment` represents the number of instances to add \(if `ScalingAdjustment` is positive\) or delete \(if it is negative\)\. In this example, `ScalingAdjustment` is 1; therefore, the policy increments the number of EC2 instances in the group by 1 when the alarm threshold is breached\.

The [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html) resource CPUAlarmHigh specifies the scaling policy ScaleUpPolicy as the action to run when the alarm is in an `ALARM` state \(`AlarmActions`\)\.

### JSON<a name="quickref-autoscaling-example-3.json"></a>

```
 1. "ScaleUpPolicy" : {
 2.    "Type" : "AWS::AutoScaling::ScalingPolicy",
 3.    "Properties" : {
 4.       "AdjustmentType" : "ChangeInCapacity",
 5.       "AutoScalingGroupName" : { "Ref" : "asGroup" },
 6.       "Cooldown" : "1",
 7.       "ScalingAdjustment" : "1"
 8.    }
 9. },
10. "CPUAlarmHigh": {
11.    "Type": "AWS::CloudWatch::Alarm",
12.    "Properties": {
13.       "EvaluationPeriods": "1",
14.       "Statistic": "Average",
15.       "Threshold": "10",
16.       "AlarmDescription": "Alarm if CPU too high or metric disappears indicating instance is down",
17.       "Period": "60",
18.       "AlarmActions": [ { "Ref": "ScaleUpPolicy" } ],
19.       "Namespace": "AWS/EC2",
20.       "Dimensions": [ {
21.          "Name": "AutoScalingGroupName",
22.          "Value": { "Ref": "asGroup" }
23.       } ],
24.       "ComparisonOperator": "GreaterThanThreshold",
25.       "MetricName": "CPUUtilization"
26.    }
27. }
```

### YAML<a name="quickref-autoscaling-example-3.yaml"></a>

```
 1. ScaleUpPolicy:
 2.   Type: AWS::AutoScaling::ScalingPolicy
 3.   Properties:
 4.     AdjustmentType: ChangeInCapacity
 5.     AutoScalingGroupName:
 6.       Ref: asGroup
 7.     Cooldown: '1'
 8.     ScalingAdjustment: '1'
 9. CPUAlarmHigh:
10.   Type: AWS::CloudWatch::Alarm
11.   Properties:
12.     EvaluationPeriods: '1'
13.     Statistic: Average
14.     Threshold: '10'
15.     AlarmDescription: Alarm if CPU too high or metric disappears indicating instance
16.       is down
17.     Period: '60'
18.     AlarmActions:
19.     - Ref: ScaleUpPolicy
20.     Namespace: AWS/EC2
21.     Dimensions:
22.     - Name: AutoScalingGroupName
23.       Value:
24.         Ref: asGroup
25.     ComparisonOperator: GreaterThanThreshold
26.     MetricName: CPUUtilization
```

### See also<a name="w6640ab1c19c22c15c15c11"></a>

For example templates for the `TargetTrackingScaling` and `StepScaling` policy types, see [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html)\.

## Declaring an Auto Scaling group with notifications<a name="scenario-as-notification"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource that sends Amazon SNS notifications when the specified events take place\. The `NotificationConfigurations` property specifies the SNS topic where AWS CloudFormation sends a notification and the events that will cause AWS CloudFormation to send notifications\. When the events specified by `NotificationTypes` occur, AWS CloudFormation will send a notification to the SNS topic specified by `TopicARN`\. In this example, AWS CloudFormation sends a notification to the SNS topic topic1 when the `autoscaling:EC2_INSTANCE_LAUNCH` and `autoscaling:EC2_INSTANCE_LAUNCH_ERROR` events occur\.

### JSON<a name="quickref-autoscaling-example-4.json"></a>

```
 1. "MyAsGroupWithNotification" : {
 2.   "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.   "Properties" : {
 4.     "AvailabilityZones" : { "Ref" : "azList" },
 5.     "LaunchConfigurationName" : { "Ref" : "myLCOne" },
 6.     "MinSize" : "0",
 7.     "MaxSize" : "2",
 8.     "DesiredCapacity" : "1",
 9.     "NotificationConfigurations" : [
10.       {
11.         "TopicARN" : { "Ref" : "topic1" },
12.         "NotificationTypes" : [
13.           "autoscaling:EC2_INSTANCE_LAUNCH",
14.           "autoscaling:EC2_INSTANCE_LAUNCH_ERROR",
15.           "autoscaling:EC2_INSTANCE_TERMINATE",
16.           "autoscaling:EC2_INSTANCE_TERMINATE_ERROR"
17.         ]
18.       }
19.     ]
20.   }
21. }
```

### YAML<a name="quickref-autoscaling-example-4.yaml"></a>

```
 1. MyAsGroupWithNotification:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   Properties:
 4.     AvailabilityZones:
 5.       Ref: azList
 6.     LaunchConfigurationName:
 7.       Ref: myLCOne
 8.     MinSize: '0'
 9.     MaxSize: '2'
10.     DesiredCapacity: '1'
11.     NotificationConfigurations:
12.     - TopicARN:
13.         Ref: topic1
14.       NotificationTypes:
15.       - autoscaling:EC2_INSTANCE_LAUNCH
16.       - autoscaling:EC2_INSTANCE_LAUNCH_ERROR
17.       - autoscaling:EC2_INSTANCE_TERMINATE
18.       - autoscaling:EC2_INSTANCE_TERMINATE_ERROR
```

## Declaring an Auto Scaling group with an UpdatePolicy<a name="scenario-as-updatepolicy"></a>

This example shows how to use an [UpdatePolicy attribute](aws-attribute-updatepolicy.md) with an Auto Scaling group\.

### JSON<a name="quickref-autoscaling-example-5.json"></a>

```
"ASG1" : {
   "UpdatePolicy" : {
      "AutoScalingRollingUpdate" : {
         "MinInstancesInService" : "1",
         "MaxBatchSize" : "1",
         "PauseTime" : "PT12M5S"
      }
   },
   "Type" : "AWS::AutoScaling::AutoScalingGroup",
   "Properties" : {
      "AvailabilityZones" : { "Fn::GetAZs" : { "Ref" : "AWS::Region" } },
      "LaunchConfigurationName" : { "Ref" : "ASLC" },
      "MaxSize" : "3",
      "MinSize" : "1"
   }
}
```

### YAML<a name="quickref-autoscaling-example-5.yaml"></a>

```
ASG1:
  UpdatePolicy:
    AutoScalingRollingUpdate:
      MinInstancesInService: '1'
      MaxBatchSize: '1'
      PauseTime: PT12M5S
  Type: AWS::AutoScaling::AutoScalingGroup
  Properties:
    AvailabilityZones:
      Fn::GetAZs:
        Ref: AWS::Region
    LaunchConfigurationName:
      Ref: ASLC
    MaxSize: '3'
    MinSize: '1'
```

## Application Auto Scaling template examples<a name="scenario-app-as-template-examples"></a>

This section provides AWS CloudFormation template examples for Application Auto Scaling scaling policies and scheduled actions for different AWS resources\. 

**Topics**
+ [Declaring a scaling policy for an Aurora DB cluster](#w6640ab1c19c22c15c21c11)
+ [Declaring a scaling policy for a DynamoDB table](#w6640ab1c19c22c15c21c13)
+ [Declaring a scaling policy for an Amazon ECS service](#w6640ab1c19c22c15c21c15)
+ [Declaring a scheduled action for a Lambda function](#w6640ab1c19c22c15c21c17)
+ [Declaring a scheduled action for a Spot Fleet](#w6640ab1c19c22c15c21c19)

**Important**  
When an Application Auto Scaling snippet is included in the template, you should declare a dependency on the specific scalable resource that is created through the template using the [DependsOn](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) attribute\. This overrides the default parallelism and directs AWS CloudFormation to operate on resources in a specified order\. Otherwise, the scaling configuration might be applied before the resource has been set up completely\.

### Declaring a scaling policy for an Aurora DB cluster<a name="w6640ab1c19c22c15c21c11"></a>

In this snippet, you register an [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html) resource named my\-db\-cluster\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource indicates that the DB cluster should be dynamically scaled to have from one to eight Aurora Replicas\. You also apply a target tracking scaling policy named AuroraScalingPolicy to the cluster using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. 

In this configuration, the `RDSReaderAverageCPUUtilization` predefined metric is used to adjust an Aurora DB cluster based on an average CPU utilization of 40 percent across all Aurora Replicas in that Aurora DB cluster\. The configuration provides a scale\-in cooldown period of 10 minutes and a scale\-out cooldown period of 5 minutes\.

#### JSON<a name="quickref-autoscaling-example-7.json"></a>

```
{
  "Resources":{
    "ScalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
        "MaxCapacity":8,
        "MinCapacity":1,
        "RoleARN":{
          "Fn::Sub":"arn:aws:iam::${AWS::AccountId}:role/aws-service-role/rds.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_RDSCluster"
        },
        "ServiceNamespace":"rds",
        "ScalableDimension":"rds:cluster:ReadReplicaCount",
        "ResourceId":"cluster:my-db-cluster"
      }
    },
    "ScalingPolicyDBCluster":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":"AuroraScalingPolicy",
        "PolicyType":"TargetTrackingScaling",
        "ServiceNamespace":"rds",
        "ScalableDimension":"rds:cluster:ReadReplicaCount",
        "ResourceId":"cluster:my-db-cluster",
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":40,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"RDSReaderAverageCPUUtilization"
          },
          "ScaleInCooldown":600,
          "ScaleOutCooldown":300
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
      PolicyName: AuroraScalingPolicy
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

### Declaring a scaling policy for a DynamoDB table<a name="w6640ab1c19c22c15c21c13"></a>

This snippet shows how to create a policy with the `TargetTrackingScaling` policy type and apply it to an [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html) resource using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource declares a scalable target to which this policy is applied, with a minimum of five write capacity units and a maximum of 15\. The scaling policy scales the table's write capacity throughput to maintain the target utilization at 50 percent based on the write capacity utilization metric\.

**Note**  
For more information about how to create a AWS CloudFormation template for DynamoDB resources, see [How to use AWS CloudFormation to configure auto scaling for Amazon DynamoDB tables and indexes](http://aws.amazon.com/blogs/database/how-to-use-aws-cloudformation-to-configure-auto-scaling-for-amazon-dynamodb-tables-and-indexes/)\.

#### JSON<a name="quickref-autoscaling-example-8.json"></a>

```
{
  "Resources":{
    "WriteCapacityScalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
        "MaxCapacity":15,
        "MinCapacity":5,
        "RoleARN":{
          "Fn::Sub":"arn:aws:iam::${AWS::AccountId}:role/aws-service-role/dynamodb.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_DynamoDBTable"
        },
        "ServiceNamespace":"dynamodb",
        "ScalableDimension":"dynamodb:table:WriteCapacityUnits",
        "ResourceId":{
          "Fn::Join":[
            "/",
            [
              "table",
              {
                "Ref":"DDBTable"
              }
            ]
          ]
        }
      }
    },
    "WriteScalingPolicy":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":"WriteScalingPolicy",
        "PolicyType":"TargetTrackingScaling",
        "ScalingTargetId":{
          "Ref":"WriteCapacityScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":50.0,
          "ScaleInCooldown":60,
          "ScaleOutCooldown":60,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"DynamoDBWriteCapacityUtilization"
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
          - !Ref DDBTable
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

### Declaring a scaling policy for an Amazon ECS service<a name="w6640ab1c19c22c15c21c15"></a>

This snippet shows how to create a policy and apply it to an [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html) resource using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource declares a scalable target to which this policy is applied\. Application Auto Scaling can scale the number of tasks at a minimum of 1 task and a maximum of 2\.

This example creates two scaling policies with the `TargetTrackingScaling` policy type\. The policies are used to scale the ECS service based on the service's average CPU and memory usage\. 

#### JSON<a name="quickref-autoscaling-example-9.json"></a>

```
{
  "Resources":{
    "ECSScalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
        "MaxCapacity":"2",
        "MinCapacity":"1",
        "RoleARN":{
          "Fn::Sub":"arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ecs.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_ECSService"
        },
        "ServiceNamespace":"ecs",
        "ScalableDimension":"ecs:service:DesiredCount",
        "ResourceId":{
          "Fn::Join":[
            "/",
            [
              "service",
              {
                "Ref":"cluster"
              },
              {
                "Fn::GetAtt":[
                  "service",
                  "Name"
                ]
              }
            ]
          ]
        }
      }
    },
    "ServiceScalingPolicyCPU":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":{"Fn::Sub":"${AWS::StackName}-target-tracking-cpu70"},
        "PolicyType":"TargetTrackingScaling",
        "ScalingTargetId":{
          "Ref":"ECSScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":70.0,
          "ScaleInCooldown":180,
          "ScaleOutCooldown":60,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ECSServiceAverageCPUUtilization"
          }
        }
      }
    },
    "ServiceScalingPolicyMem":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":{"Fn::Sub":"${AWS::StackName}-target-tracking-mem90"},
        "PolicyType":"TargetTrackingScaling",
        "ScalingTargetId":{
          "Ref":"ECSScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":90.0,
          "ScaleInCooldown":180,
          "ScaleOutCooldown":60,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ECSServiceAverageMemoryUtilization"
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
          - !Ref cluster
          - !GetAtt service.Name
  ServiceScalingPolicyCPU:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: !Sub ${AWS::StackName}-target-tracking-cpu70
      PolicyType: TargetTrackingScaling
      ScalingTargetId:
        Ref: ECSScalableTarget
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
      ScalingTargetId:
        Ref: ECSScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 90.0
        ScaleInCooldown: 180
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: ECSServiceAverageMemoryUtilization
```

The following [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource applies a target tracking scaling policy with the `ALBRequestCountPerTarget` predefined metric to an ECS service named `web-app` in the default cluster\. The policy is used to add capacity to the ECS service when the request count per target exceeds the target value\. Because the value of `DisableScaleIn` is set to true, the target tracking policy won't remove capacity from the scalable target\.

#### JSON<a name="quickref-autoscaling-example-10.json"></a>

```
{
  "Resources":{
    "ServiceScalingPolicyALB":{
      "Type":"AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties":{
        "PolicyName":"alb-scale-out-target-tracking-scaling-policy",
        "PolicyType":"TargetTrackingScaling",
        "ServiceNamespace":"ecs",
        "ScalableDimension":"ecs:service:DesiredCount",
        "ResourceId":"service/default/web-app",
        "TargetTrackingScalingPolicyConfiguration":{
          "TargetValue":1000.0,
          "ScaleInCooldown":60,
          "ScaleOutCooldown":60,
          "DisableScaleIn":true,
          "PredefinedMetricSpecification":{
            "PredefinedMetricType":"ALBRequestCountPerTarget",
            "ResourceLabel": "app/EC2Co-EcsEl-1TKLTMITMM0EO/f37c06a68c1748aa/targetgroup/EC2Co-Defau-LDNM7Q3ZH1ZN/6d4ea56ca2d6a18d"
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
  ServiceScalingPolicyALB:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: alb-scale-out-target-tracking-scaling-policy
      PolicyType: TargetTrackingScaling
      ServiceNamespace: ecs
      ScalableDimension: ecs:service:DesiredCount
      ResourceId: service/default/web-app
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 1000.0
        ScaleInCooldown: 60
        ScaleOutCooldown: 60
        DisableScaleIn: true
        PredefinedMetricSpecification:
          PredefinedMetricType: ALBRequestCountPerTarget
          ResourceLabel: app/EC2Co-EcsEl-1TKLTMITMM0EO/f37c06a68c1748aa/targetgroup/EC2Co-Defau-LDNM7Q3ZH1ZN/6d4ea56ca2d6a18d
```

### Declaring a scheduled action for a Lambda function<a name="w6640ab1c19c22c15c21c17"></a>

This snippet registers the provisioned concurrency for a function alias \([AWS::Lambda::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-alias.html)\) named BLUE, with a minimum capacity of 1 and a maximum capacity of 100, using the [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource\. It also creates a scheduled action with a recurring schedule using a cron expression\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions in the `RoleARN` property to specify the ARN of the service\-linked role\. It uses the [Fn::Sub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html) intrinsic function to construct the `ResourceId` property\. 

Note: You can't allocate provisioned concurrency on an alias that points to the unpublished version \($LATEST\)\. 

#### JSON<a name="quickref-autoscaling-example-11.json"></a>

```
{
  "ScalableTarget":{
    "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
    "Properties":{
      "MaxCapacity":100,
      "MinCapacity":1,
      "RoleARN":{
        "Fn::Join":[
          ":",
          [
            "arn:aws:iam:",
            {
              "Ref":"AWS::AccountId"
            },
            "role/aws-service-role/lambda.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_LambdaConcurrency"
          ]
        ]
      },
      "ServiceNamespace":"lambda",
      "ScalableDimension":"lambda:function:ProvisionedConcurrency",
      "ResourceId":{
        "Fn::Sub":"function:${MyFunction}:BLUE"
      },
      "ScheduledActions":[
        {
          "EndTime":"2019-12-31T12:00:00.000Z",
          "ScalableTargetAction":{
            "MaxCapacity":"500",
            "MinCapacity":"50"
          },
          "ScheduledActionName":"First",
          "StartTime":"2019-12-25T12:00:00.000Z",
          "Schedule":"cron(0 18 * * ? *)"
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
    MaxCapacity: 100
    MinCapacity: 1
    RoleARN: !Join 
      - ':'
      - - 'arn:aws:iam:'
        - !Ref 'AWS::AccountId'
        - role/aws-service-role/lambda.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_LambdaConcurrency
    ServiceNamespace: lambda
    ScalableDimension: lambda:function:ProvisionedConcurrency
    ResourceId: !Sub function:${MyFunction}:BLUE
    ScheduledActions:
      - EndTime: '2019-12-31T12:00:00.000Z'
        ScalableTargetAction:
          MaxCapacity: '500'
          MinCapacity: '50'
        ScheduledActionName: First
        StartTime: '2019-12-25T12:00:00.000Z'
        Schedule: 'cron(0 18 * * ? *)'
```

### Declaring a scheduled action for a Spot Fleet<a name="w6640ab1c19c22c15c21c19"></a>

This snippet shows how to create a scheduled action and apply it to an [AWS::EC2::SpotFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-spotfleet.html) resource using the [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource\. It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property\. 

#### JSON<a name="quickref-autoscaling-example-12.json"></a>

```
{
  "Resources":{
    "SpotFleetScalableTarget":{
      "Type":"AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties":{
        "MaxCapacity":2,
        "MinCapacity":1,
        "RoleARN":{
          "Fn::Sub":"arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ec2.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_EC2SpotFleetRequest"
        },
        "ServiceNamespace":"ec2",
        "ScalableDimension":"ec2:spot-fleet-request:TargetCapacity",
        "ResourceId":{
          "Fn::Join":[
            "/",
            [
              "spot-fleet-request",
              {
                "Ref":"ECSSpotFleet"
              }
            ]
          ]
        },
        "ScheduledActions":[
          {
            "EndTime":"2019-12-31T12:00:00.000Z",
            "ScalableTargetAction":{
              "MaxCapacity":"20",
              "MinCapacity":"5"
            },
            "ScheduledActionName":"First",
            "StartTime":"2019-12-25T12:00:00.000Z",
            "Schedule":"cron(0 18 * * ? *)"
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
      MaxCapacity: 2
      MinCapacity: 1
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/ec2.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_EC2SpotFleetRequest'
      ServiceNamespace: ec2
      ScalableDimension: 'ec2:spot-fleet-request:TargetCapacity'
      ResourceId: !Join 
        - /
        - - spot-fleet-request
          - !Ref ECSSpotFleet
      ScheduledActions:
        - EndTime: '2019-12-31T12:00:00.000Z'
          ScalableTargetAction:
            MaxCapacity: '20'
            MinCapacity: '5'
          ScheduledActionName: First
          StartTime: '2019-12-25T12:00:00.000Z'
          Schedule: 'cron(0 18 * * ? *)'
```