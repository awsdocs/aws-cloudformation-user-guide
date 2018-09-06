# Auto Scaling Template Snippets<a name="quickref-autoscaling"></a>

**Topics**
+ [Auto Scaling Launch Configuration Resource](#scenario-as-launch-config)
+ [Auto Scaling Group Resource](#scenario-as-group)
+ [Auto Scaling Policy Triggered by CloudWatch Alarm](#scenario-as-policy)
+ [Auto Scaling Group with Notifications](#scenario-as-notification)
+ [Auto Scaling with an UpdatePolicy](#w3ab2c17c24c15c13)

## Auto Scaling Launch Configuration Resource<a name="scenario-as-launch-config"></a>

This example shows an Auto Scaling AWS::AutoScaling::LaunchConfiguration resource\. The SecurityGroups property specifies both an AWS::EC2::SecurityGroup resource named myEC2SecurityGroup and an existing EC2 security group named myExistingEC2SecurityGroup\. The BlockDeviceMappings property lists two devices: a 50 gigabyte EBS volume mapped to /dev/sdk and a virtual device ephemeral0 mapped to /dev/sdc\. 

### JSON<a name="quickref-autoscaling-example-1.json"></a>

```
 1. "SimpleConfig" : {
 2.    "Type" : "AWS::AutoScaling::LaunchConfiguration",
 3.    "Properties" : {
 4.       "ImageId" : "ami-6411e20d",
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
 4.     ImageId: ami-6411e20d
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

## Auto Scaling Group Resource<a name="scenario-as-group"></a>

This example shows an Auto Scaling [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) resource\. The AvailabilityZones property specifies the availability zones where the auto\-scaling group's EC2 instances will be created\. In this example, the [Fn::GetAZs](intrinsic-function-reference-getavailabilityzones.md) function call `{ "Fn::GetAZs" : "" }` specifies all availability zones for the region in which the stack is created\. The LoadBalancerNames property lists the LoadBalancers used to route traffic to the Auto Scaling group\. In this example, one LoadBalancer is specified, the [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) resource LB\.

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

## Auto Scaling Policy Triggered by CloudWatch Alarm<a name="scenario-as-policy"></a>

This example shows an [AWS::AutoScaling::ScalingPolicy](aws-properties-as-policy.md) resource that scales up the Auto Scaling group asGroup\. The `AdjustmentType` property specifies ChangeInCapacity, which means that the `ScalingAdjustment` represents the number of instances to add \(if `ScalingAdjustment` is positive\) or delete \(if it is negative\)\. In this example, `ScalingAdjustment` is 1; therefore, the policy increments the number of EC2 instances in the group by 1 when the policy is executed\.

The [AWS::CloudWatch::Alarm](aws-properties-cw-alarm.md) resource CPUAlarmHigh specifies the scaling policy ScaleUpPolicy as the action to execute when the alarm is in an `ALARM` state \(`AlarmActions`\)\.

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

## Auto Scaling Group with Notifications<a name="scenario-as-notification"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) resource that sends Amazon SNS notifications when the specified events take place\. The `NotificationConfigurations` property specifies the SNS topic where AWS CloudFormation sends a notification and the events that will cause AWS CloudFormation to send notifications\. When the events specified by `NotificationTypes` occur, AWS CloudFormation will send a notification to the SNS topic specified by `TopicARN`\. In this example, AWS CloudFormation sends a notification to the SNS topic topic1 when the `autoscaling:EC2_INSTANCE_LAUNCH` and `autoscaling:EC2_INSTANCE_LAUNCH_ERROR` events occur\.

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

## Auto Scaling with an UpdatePolicy<a name="w3ab2c17c24c15c13"></a>

This example shows how to use an [UpdatePolicy](aws-attribute-updatepolicy.md) with an auto\-scaling group\.

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