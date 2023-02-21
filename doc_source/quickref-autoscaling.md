# Auto scaling template snippets<a name="quickref-autoscaling"></a>

The following examples show different snippets to include in templates for use with Amazon EC2 Auto Scaling or Application Auto Scaling\.

Amazon EC2 Auto Scaling enables you to automatically scale Amazon EC2 instances, either with scaling policies or with scheduled scaling\. Auto Scaling groups are collections of Amazon EC2 instances that enable automatic scaling and fleet management features, such as health checks and integration with Elastic Load Balancing\. 

Application Auto Scaling provides automatic scaling of different resources beyond Amazon EC2, either with scaling policies or with scheduled scaling\.

**Topics**
+ [Declaring a launch template with user data and an IAM Role](#scenario-as-launch-template)
+ [Declaring a single instance Auto Scaling group](#scenario-single-instance-as-group)
+ [Declaring an Auto Scaling group with an attached load balancer](#scenario-as-group)
+ [Declaring an Auto Scaling group with notifications](#scenario-as-notification)
+ [Declaring an Auto Scaling group with a CreationPolicy and an UpdatePolicy](#scenario-as-updatepolicy)
+ [Declaring a step scaling policy with a CloudWatch alarm](#scenario-as-policy)
+ [Mixed instances group examples](#scenario-mixed-instances-group-template-examples)
+ [Launch configuration examples](#scenario-launch-config-template-examples)
+ [Application Auto Scaling template examples](#scenario-app-as-template-examples)

## Declaring a launch template with user data and an IAM Role<a name="scenario-as-launch-template"></a>

This snippet shows an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource that contains the instance configuration information for an Auto Scaling group\. You specify values for the `ImageId`, `InstanceType`, `SecurityGroups`, `UserData`, and `TagSpecifications` properties\. The `SecurityGroups` property specifies an existing EC2 security group named `myExistingEC2SecurityGroup` and a new security group\. The [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function gets the name of the [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resource `myNewEC2SecurityGroup` that's declared elsewhere in the stack template\. 

The launch template includes a section for custom user data\. You can pass in configuration tasks and scripts that run when an instance launches in this section\. In this example, the user data installs the AWS Systems Manager Agent and starts the agent\.

The launch template also includes an IAM role that allows applications running on instances in your Auto Scaling group to perform actions on your behalf\. This example shows an [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html) resource for the launch template, which uses the `IamInstanceProfile` property to specify the IAM role\. The [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) function gets the name of the [AWS::IAM::InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html) resource `myInstanceProfile`\. To configure the permissions of the IAM role, you specify a value for the `ManagedPolicyArns` property\.

### JSON<a name="quickref-launch-template-example-1.json"></a>

```
 1. {
 2.   "Resources":{
 3.     "myLaunchTemplate":{
 4.       "Type":"AWS::EC2::LaunchTemplate",
 5.       "Properties":{
 6.         "LaunchTemplateName":{ "Fn::Sub": "${AWS::StackName}-launch-template" },
 7.         "LaunchTemplateData":{
 8.           "ImageId":"ami-02354e95b3example",
 9.           "InstanceType":"t3.micro",
10.           "IamInstanceProfile":{
11.             "Name":{
12.               "Ref":"myInstanceProfile"
13.             }
14.           },
15.           "SecurityGroups":[
16.             {
17.               "Ref":"myNewEC2SecurityGroup"
18.             },
19.             "myExistingEC2SecurityGroup"
20.           ],
21.           "UserData":{
22.             "Fn::Base64":{
23.               "Fn::Join": [
24.                 "", [
25.                   "#!/bin/bash\n",
26.                   "cd /tmp\n",
27.                   "sudo yum install -y https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/latest/linux_amd64/amazon-ssm-agent.rpm\n",
28.                   "sudo systemctl enable amazon-ssm-agent\n",
29.                   "sudo systemctl start amazon-ssm-agent\n"
30.                 ]
31.               ]
32.             }
33.           },
34.           "TagSpecifications":[
35.             {
36.               "ResourceType":"instance",
37.               "Tags":[
38.                 {
39.                   "Key":"environment",
40.                   "Value":"development"
41.                 }
42.               ]
43.             },
44.             {
45.               "ResourceType":"volume",
46.               "Tags":[
47.                 {
48.                   "Key":"environment",
49.                   "Value":"development"
50.                 }
51.               ]
52.             }
53.           ]
54.         }
55.       }
56.     },
57.     "myInstanceRole":{
58.       "Type":"AWS::IAM::Role",
59.       "Properties":{
60.         "RoleName":"InstanceRole",
61.         "AssumeRolePolicyDocument":{
62.           "Version":"2012-10-17",
63.           "Statement":[
64.             {
65.               "Effect":"Allow",
66.               "Principal":{
67.                 "Service":[
68.                   "ec2.amazonaws.com"
69.                 ]
70.               },
71.               "Action":[
72.                 "sts:AssumeRole"
73.               ]
74.             }
75.           ]
76.         },
77.         "ManagedPolicyArns":[
78.           "arn:aws:iam::aws:policy/myCustomerManagedPolicy"
79.         ]
80.       }
81.     },
82.     "myInstanceProfile":{
83.       "Type":"AWS::IAM::InstanceProfile",
84.       "Properties":{
85.         "Path":"/",
86.         "Roles":[
87.           {
88.             "Ref":"myInstanceRole"
89.           }
90.         ]
91.       }
92.     }
93.   }
94. }
```

### YAML<a name="quickref-launch-template-example-1.yaml"></a>

```
 1. ---
 2. Resources:
 3.   myLaunchTemplate:
 4.     Type: AWS::EC2::LaunchTemplate
 5.     Properties:
 6.       LaunchTemplateName: !Sub ${AWS::StackName}-launch-template
 7.       LaunchTemplateData:
 8.         ImageId: ami-02354e95b3example
 9.         InstanceType: t3.micro
10.         IamInstanceProfile:
11.           Name: !Ref myInstanceProfile
12.         SecurityGroups:
13.         - Ref! myNewEC2SecurityGroup
14.         - myExistingEC2SecurityGroup
15.         UserData:
16.           Fn::Base64:!Sub |
17.             #!/bin/bash
18.             cd /tmp
19.             sudo yum install -y https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/latest/linux_amd64/amazon-ssm-agent.rpm
20.             sudo systemctl enable amazon-ssm-agent
21.             sudo systemctl start amazon-ssm-agent
22.         TagSpecifications:
23.         - ResourceType: instance
24.           Tags:
25.           - Key: environment
26.             Value: development
27.         - ResourceType: volume
28.           Tags:
29.           - Key: environment
30.             Value: development
31.   myInstanceRole:
32.     Type: AWS::IAM::Role
33.     Properties:
34.       RoleName: InstanceRole
35.       AssumeRolePolicyDocument:
36.         Version: '2012-10-17'
37.         Statement:
38.         - Effect: 'Allow'
39.           Principal:
40.             Service:
41.             - 'ec2.amazonaws.com'
42.           Action:
43.           - 'sts:AssumeRole'
44.       ManagedPolicyArns:
45.         - 'arn:aws:iam::aws:policy/myCustomerManagedPolicy'
46.   myInstanceProfile:
47.     Type: AWS::IAM::InstanceProfile
48.     Properties:
49.       Path: '/'
50.       Roles:
51.       - !Ref myInstanceRole
```

### See also<a name="scenario-as-group-see-also"></a>

For more examples of launch templates, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#aws-resource-ec2-launchtemplate--examples) section in the `AWS::EC2::LaunchTemplate` resource and the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#aws-properties-as-group--examples) section in the `AWS::AutoScaling::AutoScalingGroup` resource\.

## Declaring a single instance Auto Scaling group<a name="scenario-single-instance-as-group"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource with a single instance to help you get started\. The `VPCZoneIdentifier` property of the Auto Scaling group specifies a list of existing subnets in three different Availability Zones\. You must specify the applicable subnet IDs from your account before you create your stack\. The `LaunchTemplate` property references an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource with the logical name `myLaunchTemplate` that is defined elsewhere in your template\.

### JSON<a name="quickref-autoscaling-example-1.json"></a>

```
 1. "myASG" : {
 2.    "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.    "Properties" : {
 4.       "VPCZoneIdentifier" : [ "subnetIdAz1", "subnetIdAz2", "subnetIdAz3" ],
 5.       "LaunchTemplate" : {
 6.         "LaunchTemplateId" : {
 7.           "Ref" : "myLaunchTemplate"
 8.         },
 9.         "Version" : {
10.           "Fn::GetAtt" : [
11.             "myLaunchTemplate",
12.             "LatestVersionNumber"
13.           ]
14.         }
15.       },
16.       "MaxSize" : "1",
17.       "MinSize" : "0",
18.       "DesiredCapacity" : "1"
19.    }
20. }
```

### YAML<a name="quickref-autoscaling-example-1.yaml"></a>

```
 1. myASG:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   Properties:
 4.     VPCZoneIdentifier:
 5.     - subnetIdAz1
 6.     - subnetIdAz2
 7.     - subnetIdAz3
 8.     LaunchTemplate:
 9.       LaunchTemplateId: !Ref myLaunchTemplate
10.       Version: !GetAtt myLaunchTemplate.LatestVersionNumber
11.     MaxSize: '1'
12.     MinSize: '0'
13.     DesiredCapacity: '1'
```

## Declaring an Auto Scaling group with an attached load balancer<a name="scenario-as-group"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource for load balancing over multiple servers\. It specifies the logical names of AWS resources declared elsewhere in the same template\.

1. The `VPCZoneIdentifier` property specifies the logical names of two [AWS::EC2::Subnet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html) resources where the Auto Scaling group's EC2 instances will be created: `myPublicSubnet1` and `myPublicSubnet2`\.

1. The `LaunchTemplate` property specifies an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource with the logical name `myLaunchTemplate`\.

1. The `TargetGroupARNs` property lists the target groups for an Application Load Balancer or Network Load Balancer used to route traffic to the Auto Scaling group\. In this example, one target group is specified, an [AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html) resource with the logical name `myTargetGroup`\.

### JSON<a name="quickref-autoscaling-example-2.json"></a>

```
 1. "myServerGroup" : {
 2.    "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.    "Properties" : {
 4.       "VPCZoneIdentifier" : [ { "Ref" : "myPublicSubnet1" }, { "Ref" : "myPublicSubnet2" } ],
 5.       "LaunchTemplate" : {
 6.         "LaunchTemplateId" : {
 7.           "Ref" : "myLaunchTemplate"
 8.         },
 9.         "Version" : {
10.           "Fn::GetAtt" : [
11.             "myLaunchTemplate",
12.             "LatestVersionNumber"
13.           ]
14.         }
15.       },
16.       "MaxSize" : "5",
17.       "MinSize" : "1",
18.       "TargetGroupARNs" : [ { "Ref" : "myTargetGroup" } ]
19.    }
20. }
```

### YAML<a name="quickref-autoscaling-example-2.yaml"></a>

```
 1. myServerGroup:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   Properties:
 4.     VPCZoneIdentifier:
 5.       - !Ref myPublicSubnet1
 6.       - !Ref myPublicSubnet2
 7.     LaunchTemplate:
 8.       LaunchTemplateId: !Ref myLaunchTemplate
 9.       Version: !GetAtt myLaunchTemplate.LatestVersionNumber
10.     MaxSize: '5'
11.     MinSize: '1'
12.     TargetGroupARNs:
13.       - !Ref myTargetGroup
```

### See also<a name="scenario-as-group-see-also"></a>

For a detailed example that creates an Auto Scaling group with a target tracking scaling policy based on the `ALBRequestCountPerTarget` predefined metric for your Application Load Balancer, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscaling-scalingpolicy.html#aws-resource-autoscaling-scalingpolicy--examples) section in the `AWS::AutoScaling::ScalingPolicy` resource\.

## Declaring an Auto Scaling group with notifications<a name="scenario-as-notification"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource that sends Amazon SNS notifications when the specified events take place\. The `NotificationConfigurations` property specifies the SNS topic where AWS CloudFormation sends a notification and the events that will cause AWS CloudFormation to send notifications\. When the events specified by `NotificationTypes` occur, AWS CloudFormation will send a notification to the SNS topic specified by `TopicARN`\. When you launch the stack, AWS CloudFormation creates an [AWS::SNS::Subscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sns-subscription.html) resource \(`snsTopicForAutoScalingGroup`\) that's declared within the same template\.

The `VPCZoneIdentifier` property of the Auto Scaling group specifies a list of existing subnets in three different Availability Zones\. You must specify the applicable subnet IDs from your account before you create your stack\. The `LaunchTemplate` property references the logical name of an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource declared elsewhere in the same template\.

### JSON<a name="quickref-autoscaling-example-3.json"></a>

```
 1. "myASG" : {
 2.   "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.   "DependsOn": [
 4.     "snsTopicForAutoScalingGroup"
 5.   ],
 6.   "Properties" : {
 7.     "VPCZoneIdentifier" : [ "subnetIdAz1", "subnetIdAz2", "subnetIdAz3" ],
 8.     "LaunchTemplate" : {
 9.       "LaunchTemplateId" : {
10.         "Ref" : "logicalName"
11.       },
12.       "Version" : {
13.         "Fn::GetAtt" : [
14.           "logicalName",
15.           "LatestVersionNumber"
16.         ]
17.       }
18.     },
19.     "MaxSize" : "5",
20.     "MinSize" : "1",
21.     "NotificationConfigurations" : [
22.       {
23.         "TopicARN" : { "Ref" : "snsTopicForAutoScalingGroup" },
24.         "NotificationTypes" : [
25.           "autoscaling:EC2_INSTANCE_LAUNCH",
26.           "autoscaling:EC2_INSTANCE_LAUNCH_ERROR",
27.           "autoscaling:EC2_INSTANCE_TERMINATE",
28.           "autoscaling:EC2_INSTANCE_TERMINATE_ERROR",
29.           "autoscaling:TEST_NOTIFICATION"
30.         ]
31.       }
32.     ]
33.   }
34. }
```

### YAML<a name="quickref-autoscaling-example-3.yaml"></a>

```
 1. myASG:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   DependsOn:
 4.     - snsTopicForAutoScalingGroup
 5.   Properties:
 6.     VPCZoneIdentifier:
 7.     - subnetIdAz1
 8.     - subnetIdAz2
 9.     - subnetIdAz3
10.     LaunchTemplate:
11.       LaunchTemplateId: !Ref logicalName
12.       Version: !GetAtt logicalName.LatestVersionNumber
13.     MaxSize: '5'
14.     MinSize: '1'
15.     NotificationConfigurations:
16.     - TopicARN: !Ref snsTopicForAutoScalingGroup
17.       NotificationTypes:
18.       - autoscaling:EC2_INSTANCE_LAUNCH
19.       - autoscaling:EC2_INSTANCE_LAUNCH_ERROR
20.       - autoscaling:EC2_INSTANCE_TERMINATE
21.       - autoscaling:EC2_INSTANCE_TERMINATE_ERROR
22.       - autoscaling:TEST_NOTIFICATION
```

## Declaring an Auto Scaling group with a CreationPolicy and an UpdatePolicy<a name="scenario-as-updatepolicy"></a>

The following example shows how to add [`CreationPolicy`](aws-attribute-creationpolicy.md) and [`UpdatePolicy`](aws-attribute-updatepolicy.md) attributes to an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource\.

The sample creation policy prevents the Auto Scaling group from reaching `CREATE_COMPLETE` status until AWS CloudFormation receives `Count` number of success signals when the group is ready\. To signal that the Auto Scaling group is ready, a [cfn\-signal](cfn-signal.md) helper script added to the launch template's user data \(not shown\) is run on the instances\. If the instances don't send a signal within the specified `Timeout`, CloudFormation assumes that the instances were not created, the resource creation fails, and CloudFormation rolls the stack back\.

The sample update policy instructs CloudFormation to perform a rolling update using the `AutoScalingRollingUpdate` property\. The rolling update makes changes to the Auto Scaling group in small batches \(for this example, instance by instance\) based on the `MaxBatchSize` and a pause time between batches of updates based on the `PauseTime`\. The `MinInstancesInService` attribute specifies the minimum number of instances that must be in service within the Auto Scaling group while CloudFormation updates old instances\.

The `WaitOnResourceSignals` attribute is set to `true`\. CloudFormation must receive a signal from each new instance within the specified `PauseTime` before continuing the update\. While the stack update is in progress, the following EC2 Auto Scaling processes are suspended: `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, and `ScheduledActions`\. Note: Don't suspend the `Launch`, `Terminate`, or `AddToLoadBalancer` \(if the Auto Scaling group is being used with Elastic Load Balancing\) process types because doing so can prevent the rolling update from functioning properly\.

The `VPCZoneIdentifier` property of the Auto Scaling group specifies a list of existing subnets in three different Availability Zones\. You must specify the applicable subnet IDs from your account before you create your stack\. The `LaunchTemplate` property references the logical name of an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource declared elsewhere in the same template\.

### JSON<a name="quickref-autoscaling-example-4.json"></a>

```
{
  "Resources":{
    "myASG":{
      "CreationPolicy":{
        "ResourceSignal":{
          "Count":"3",
          "Timeout":"PT15M"
        }
      },
      "UpdatePolicy":{
        "AutoScalingRollingUpdate":{
          "MinInstancesInService":"1",
          "MaxBatchSize":"1",
          "PauseTime":"PT12M5S",
          "WaitOnResourceSignals":"true",
          "SuspendProcesses":[
            "HealthCheck",
            "ReplaceUnhealthy",
            "AZRebalance",
            "AlarmNotification",
            "ScheduledActions"
          ]
        }
      },
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "VPCZoneIdentifier":[ "subnetIdAz1", "subnetIdAz2", "subnetIdAz3" ],
        "LaunchTemplate":{
          "LaunchTemplateId":{
            "Ref":"logicalName"
          },
          "Version":{
            "Fn::GetAtt":[
              "logicalName",
              "LatestVersionNumber"
            ]
          }
        },
        "MaxSize":"5",
        "MinSize":"3"
      }
    }
  }
}
```

### YAML<a name="quickref-autoscaling-example-4.yaml"></a>

```
---
Resources:
  myASG:
    CreationPolicy:
      ResourceSignal:
        Count: '3'
        Timeout: PT15M
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
      VPCZoneIdentifier:
      - subnetIdAz1
      - subnetIdAz2
      - subnetIdAz3
      LaunchTemplate:
        LaunchTemplateId: !Ref logicalName
        Version: !GetAtt logicalName.LatestVersionNumber
      MaxSize: '5'
      MinSize: '3'
```

## Declaring a step scaling policy with a CloudWatch alarm<a name="scenario-as-policy"></a>

This example shows an [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscaling-scalingpolicy.html) resource that scales out the Auto Scaling group using a step scaling policy\. The `AdjustmentType` property specifies `ChangeInCapacity`, which means that the `ScalingAdjustment` represents the number of instances to add \(if `ScalingAdjustment` is positive\) or delete \(if it is negative\)\. In this example, `ScalingAdjustment` is 1; therefore, the policy increments the number of EC2 instances in the group by 1 when the alarm threshold is breached\.

The [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html) resource `CPUAlarmHigh` specifies the scaling policy `ASGScalingPolicyHigh` as the action to run when the alarm is in an ALARM state \(`AlarmActions`\)\. The `Dimensions` property references the logical name of an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource declared elsewhere in the same template\.

### JSON<a name="quickref-autoscaling-example-5.json"></a>

```
 1. {
 2.   "Resources":{
 3.     "ASGScalingPolicyHigh":{
 4.       "Type":"AWS::AutoScaling::ScalingPolicy",
 5.       "Properties":{
 6.         "AutoScalingGroupName":{ "Ref":"logicalName" },
 7.         "PolicyType":"StepScaling",
 8.         "AdjustmentType":"ChangeInCapacity",
 9.         "StepAdjustments":[
10.           {
11.             "MetricIntervalLowerBound":0,
12.             "ScalingAdjustment":1
13.           }
14.         ]
15.       }
16.     },
17.     "CPUAlarmHigh":{
18.       "Type":"AWS::CloudWatch::Alarm",
19.       "Properties":{
20.         "EvaluationPeriods":"2",
21.         "Statistic":"Average",
22.         "Threshold":"90",
23.         "AlarmDescription":"Scale out if CPU > 90% for 2 minutes",
24.         "Period":"60",
25.         "AlarmActions":[ { "Ref":"ASGScalingPolicyHigh" } ],
26.         "Namespace":"AWS/EC2",
27.         "Dimensions":[
28.           {
29.             "Name":"AutoScalingGroupName",
30.             "Value":{ "Ref":"logicalName" }
31.           }
32.         ],
33.         "ComparisonOperator":"GreaterThanThreshold",
34.         "MetricName":"CPUUtilization"
35.       }
36.     }
37.   }
38. }
```

### YAML<a name="quickref-autoscaling-example-5.yaml"></a>

```
 1. ---
 2. Resources:
 3.   ASGScalingPolicyHigh:
 4.     Type: AWS::AutoScaling::ScalingPolicy
 5.     Properties:
 6.       AutoScalingGroupName: !Ref logicalName
 7.       PolicyType: StepScaling
 8.       AdjustmentType: ChangeInCapacity
 9.       StepAdjustments: 
10.         - MetricIntervalLowerBound: 0
11.           ScalingAdjustment: 1
12.   CPUAlarmHigh:
13.     Type: AWS::CloudWatch::Alarm
14.     Properties:
15.       EvaluationPeriods: 2
16.       Statistic: Average
17.       Threshold: 90
18.       AlarmDescription: 'Scale out if CPU > 90% for 2 minutes'
19.       Period: 60
20.       AlarmActions:
21.       - !Ref ASGScalingPolicyHigh
22.       Namespace: AWS/EC2
23.       Dimensions:
24.       - Name: AutoScalingGroupName
25.         Value:
26.           Ref! logicalName
27.       ComparisonOperator: GreaterThanThreshold
28.       MetricName: CPUUtilization
```

### See also<a name="scenario-as-policy-see-also"></a>

For more example templates for scaling policies, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscaling-scalingpolicy.html#aws-resource-autoscaling-scalingpolicy--examples) section in the `AWS::AutoScaling::ScalingPolicy` resource\.

## Mixed instances group examples<a name="scenario-mixed-instances-group-template-examples"></a>

### Declaring an Auto Scaling group that uses a mixed instances policy and attribute\-based instance type selection<a name="scenario-mixed-instances-group-instance-requirements"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource that contains the information to launch a mixed instances group using attribute\-based instance type selection\. You specify the minimum and maximum values for the `VCpuCount` property and the minimum value for the `MemoryMiB` property\. Any instance types used by the Auto Scaling group must match your required instance attributes\. 

The `VPCZoneIdentifier` property of the Auto Scaling group specifies a list of existing subnets in three different Availability Zones\. You must specify the applicable subnet IDs from your account before you create your stack\. The `LaunchTemplate` property references the logical name of an [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html) resource declared elsewhere in the same template\.

#### JSON<a name="quickref-mixed-instances-group-example-2.json"></a>

```
 1. {
 2.   "Resources":{
 3.     "myASG":{
 4.       "Type":"AWS::AutoScaling::AutoScalingGroup",
 5.       "Properties":{
 6.         "VPCZoneIdentifier":[
 7.           "subnetIdAz1",
 8.           "subnetIdAz2",
 9.           "subnetIdAz3"
10.         ],
11.         "MixedInstancesPolicy":{
12.           "LaunchTemplate":{
13.             "LaunchTemplateSpecification":{
14.               "LaunchTemplateId":{
15.                 "Ref":"logicalName"
16.               },
17.               "Version":{
18.                 "Fn::GetAtt":[
19.                   "logicalName",
20.                   "LatestVersionNumber"
21.                 ]
22.               }
23.             },
24.             "Overrides":[
25.               {
26.                 "InstanceRequirements":{
27.                   "VCpuCount":{
28.                     "Min":2,
29.                     "Max":4
30.                   },
31.                   "MemoryMiB":{
32.                     "Min":2048
33.                   }
34.                 }
35.               }
36.             ]
37.           }
38.         },
39.         "MaxSize":"5",
40.         "MinSize":"1",
41.         "DesiredCapacity":"3"
42.       }
43.     }
44.   }
45. }
```

#### YAML<a name="quickref-mixed-instances-group-example-1.yaml"></a>

```
 1. ---
 2. Resources:
 3.   myASG:
 4.     Type: AWS::AutoScaling::AutoScalingGroup
 5.     Properties:
 6.       VPCZoneIdentifier:
 7.       - subnetIdAz1
 8.       - subnetIdAz2
 9.       - subnetIdAz3
10.       MixedInstancesPolicy:
11.         LaunchTemplate:
12.           LaunchTemplateSpecification:
13.             LaunchTemplateId: !Ref logicalName
14.             Version: !GetAtt logicalName.LatestVersionNumber
15.           Overrides:
16.           - InstanceRequirements:
17.               VCpuCount:
18.                 Min: 2
19.                 Max: 4
20.               MemoryMiB:
21.                 Min: 2048
22.       MaxSize: '5'
23.       MinSize: '1'
24.       DesiredCapacity: '3'
```

## Launch configuration examples<a name="scenario-launch-config-template-examples"></a>

### Declaring a launch configuration<a name="scenario-as-launch-config"></a>

This example shows an [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscaling-launchconfiguration.html) resource for an Auto Scaling group where you specify values for the `ImageId`, `InstanceType`, and `SecurityGroups` properties\. The `SecurityGroups` property specifies both the logical name of an [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html) resource that's specified elsewhere in the template, and an existing EC2 security group named `myExistingEC2SecurityGroup`\.

#### JSON<a name="quickref-launch-config-example-1.json"></a>

```
1. "mySimpleConfig" : {
2.    "Type" : "AWS::AutoScaling::LaunchConfiguration",
3.    "Properties" : {
4.       "ImageId" : "ami-02354e95b3example",
5.       "InstanceType" : "t3.micro",
6.       "SecurityGroups" : [ { "Ref" : "logicalName" }, "myExistingEC2SecurityGroup" ]
7.    }
8. }
```

#### YAML<a name="quickref-launch-config-example-1.yaml"></a>

```
1. mySimpleConfig:
2.   Type: AWS::AutoScaling::LaunchConfiguration
3.   Properties:
4.     ImageId: ami-02354e95b3example
5.     InstanceType: t3.micro
6.     SecurityGroups:
7.     - Ref! logicalName
8.     - myExistingEC2SecurityGroup
```

### Declaring an Auto Scaling group that uses a launch configuration<a name="scenario-single-instance-as-group-launch-configuration"></a>

This example shows an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource with a single instance\. The `VPCZoneIdentifier` property of the Auto Scaling group specifies a list of existing subnets in three different Availability Zones\. You must specify the applicable subnet IDs from your account before you create your stack\. The `LaunchConfigurationName` property references an [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscaling-launchconfiguration.html) resource with the logical name `mySimpleConfig` that is defined in your template\.

#### JSON<a name="quickref-launch-config-example-2.json"></a>

```
 1. "myASG" : {
 2.    "Type" : "AWS::AutoScaling::AutoScalingGroup",
 3.    "Properties" : {
 4.       "VPCZoneIdentifier" : [ "subnetIdAz1", "subnetIdAz2", "subnetIdAz3" ],
 5.       "LaunchConfigurationName" : { "Ref" : "mySimpleConfig" },
 6.       "MaxSize" : "1",
 7.       "MinSize" : "0",
 8.       "DesiredCapacity" : "1"
 9.    }
10. }
```

#### YAML<a name="quickref-launch-config-example-2.yaml"></a>

```
 1. myASG:
 2.   Type: AWS::AutoScaling::AutoScalingGroup
 3.   Properties:
 4.     VPCZoneIdentifier:
 5.     - subnetIdAz1
 6.     - subnetIdAz2
 7.     - subnetIdAz3
 8.     LaunchConfigurationName: !Ref mySimpleConfig
 9.     MaxSize: '1'
10.     MinSize: '0'
11.     DesiredCapacity: '1'
```

## Application Auto Scaling template examples<a name="scenario-app-as-template-examples"></a>

This section provides AWS CloudFormation template examples for Application Auto Scaling scaling policies and scheduled actions for different AWS resources\.

**Topics**
+ [Declaring a scaling policy for an AppStream fleet](#w2ab1c23c21c15c33b9)
+ [Declaring a scaling policy for an Aurora DB cluster](#w2ab1c23c21c15c33c11)
+ [Declaring a scaling policy for a DynamoDB table](#w2ab1c23c21c15c33c13)
+ [Declaring a scaling policy for an Amazon ECS service \(metrics: average CPU and memory\)](#w2ab1c23c21c15c33c15)
+ [Declaring a scaling policy for an Amazon ECS service \(metric: average request count per target\)](#w2ab1c23c21c15c33c17)
+ [Declaring a scheduled action with a cron expression for a Lambda function](#w2ab1c23c21c15c33c19)
+ [Declaring a scheduled action with an `at` expression for a Spot Fleet](#w2ab1c23c21c15c33c21)

**Important**  
When an Application Auto Scaling snippet is included in the template, you might need to declare a dependency on the specific scalable resource that's created through the template using the [DependsOn](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) attribute\. This overrides the default parallelism and directs AWS CloudFormation to operate on resources in a specified order\. Otherwise, the scaling configuration might be applied before the resource has been set up completely\.

### Declaring a scaling policy for an AppStream fleet<a name="w2ab1c23c21c15c33b9"></a>

This snippet shows how to create a policy and apply it to an [AWS::AppStream::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-fleet.html) resource using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource declares a scalable target to which this policy is applied\. Application Auto Scaling can scale the number of fleet instances at a minimum of 1 instance and a maximum of 20\. The policy keeps the average capacity utilization of the fleet at 75 percent, with scale\-out and scale\-in cooldown periods of 300 seconds \(5 minutes\)\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property with the logical name of the `AWS::AppStream::Fleet` resource that's specified in the same template\.

#### JSON<a name="quickref-autoscaling-example-6.json"></a>

```
{
  "Resources" : {
    "ScalableTarget" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties" : {
        "MaxCapacity" : 20,
        "MinCapacity" : 1,
        "RoleARN" : { "Fn::Sub" : "arn:aws:iam::${AWS::AccountId}:role/aws-service-role/appstream.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_AppStreamFleet" },
        "ServiceNamespace" : "appstream",
        "ScalableDimension" : "appstream:fleet:DesiredCapacity",
        "ResourceId" : {
          "Fn::Join" : [
            "/",
            [
              "fleet",
              {
                "Ref" : "logicalName"
              }
            ]
          ]
        }
      }
    },
    "ScalingPolicyAppStreamFleet" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties" : {
        "PolicyName" : { "Fn::Sub" : "${AWS::StackName}-target-tracking-cpu75" },
        "PolicyType" : "TargetTrackingScaling",
        "ServiceNamespace" : "appstream",
        "ScalableDimension" : "appstream:fleet:DesiredCapacity",
        "ResourceId" : {
          "Fn::Join" : [
            "/",
            [
              "fleet",
              {
                "Ref" : "logicalName"
              }
            ]
          ]
        },
        "TargetTrackingScalingPolicyConfiguration" : {
          "TargetValue" : 75,
          "PredefinedMetricSpecification" : {
            "PredefinedMetricType" : "AppStreamAverageCapacityUtilization"
          },
          "ScaleInCooldown" : 300,
          "ScaleOutCooldown" : 300
        }
      }
    } 
  }
}
```

#### YAML<a name="quickref-autoscaling-example-6.yaml"></a>

```
---
Resources:
  ScalableTarget:
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: 20
      MinCapacity: 1
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/appstream.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_AppStreamFleet'
      ServiceNamespace: appstream
      ScalableDimension: appstream:fleet:DesiredCapacity
      ResourceId: !Join
        - /
        - - fleet
          - !Ref logicalName
  ScalingPolicyAppStreamFleet:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: !Sub ${AWS::StackName}-target-tracking-cpu75
      PolicyType: TargetTrackingScaling
      ServiceNamespace: appstream
      ScalableDimension: appstream:fleet:DesiredCapacity
      ResourceId: !Join
        - /
        - - fleet
          - !Ref logicalName
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 75
        PredefinedMetricSpecification:
          PredefinedMetricType: AppStreamAverageCapacityUtilization
        ScaleInCooldown: 300
        ScaleOutCooldown: 300
```

### Declaring a scaling policy for an Aurora DB cluster<a name="w2ab1c23c21c15c33c11"></a>

In this snippet, you register an [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html) resource\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource indicates that the DB cluster should be dynamically scaled to have from one to eight Aurora Replicas\. You also apply a target tracking scaling policy to the cluster using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\.

In this configuration, the `RDSReaderAverageCPUUtilization` predefined metric is used to adjust an Aurora DB cluster based on an average CPU utilization of 40 percent across all Aurora Replicas in that Aurora DB cluster\. The configuration provides a scale\-in cooldown period of 10 minutes and a scale\-out cooldown period of 5 minutes\.

This example uses the [Fn::Sub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html) intrinsic function to construct the `ResourceId` property with the logical name of the `AWS::RDS::DBCluster` resource that is specified in the same template\.

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
        "ResourceId" : { "Fn::Sub" : "cluster:${logicalName}" }
      }
    },
    "ScalingPolicyDBCluster" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties" : {
        "PolicyName" : { "Fn::Sub" : "${AWS::StackName}-target-tracking-cpu40" },
        "PolicyType" : "TargetTrackingScaling",
        "ServiceNamespace" : "rds",
        "ScalableDimension" : "rds:cluster:ReadReplicaCount",
        "ResourceId" : { "Fn::Sub" : "cluster:${logicalName}" }, 
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
    Type: AWS::ApplicationAutoScaling::ScalableTarget
    Properties:
      MaxCapacity: 8
      MinCapacity: 1
      RoleARN: 
        Fn::Sub: 'arn:aws:iam::${AWS::AccountId}:role/aws-service-role/rds.application-autoscaling.amazonaws.com/AWSServiceRoleForApplicationAutoScaling_RDSCluster'
      ServiceNamespace: rds
      ScalableDimension: rds:cluster:ReadReplicaCount
      ResourceId: !Sub cluster:${logicalName}
  ScalingPolicyDBCluster:
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
    Properties:
      PolicyName: !Sub ${AWS::StackName}-target-tracking-cpu40
      PolicyType: TargetTrackingScaling
      ServiceNamespace: rds
      ScalableDimension: rds:cluster:ReadReplicaCount
      ResourceId: !Sub cluster:${logicalName}
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 40
        PredefinedMetricSpecification:
          PredefinedMetricType: RDSReaderAverageCPUUtilization
        ScaleInCooldown: 600
        ScaleOutCooldown: 300
```

### Declaring a scaling policy for a DynamoDB table<a name="w2ab1c23c21c15c33c13"></a>

This snippet shows how to create a policy with the `TargetTrackingScaling` policy type and apply it to an [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html) resource using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource declares a scalable target to which this policy is applied, with a minimum of five write capacity units and a maximum of 15\. The scaling policy scales the table's write capacity throughput to maintain the target utilization at 50 percent based on the `DynamoDBWriteCapacityUtilization` predefined metric\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property with the logical name of the `AWS::DynamoDB::Table` resource that's specified in the same template\.

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

### Declaring a scaling policy for an Amazon ECS service \(metrics: average CPU and memory\)<a name="w2ab1c23c21c15c33c15"></a>

This snippet shows how to create a policy and apply it to an [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html) resource using the [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) resource\. The [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource declares a scalable target to which this policy is applied\. Application Auto Scaling can scale the number of tasks at a minimum of 1 task and a maximum of 6\.

It creates two scaling policies with the `TargetTrackingScaling` policy type\. The policies are used to scale the ECS service based on the service's average CPU and memory usage\. It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property with the logical names of the `AWS::ECS::Cluster` \(`myContainerCluster`\) and `AWS::ECS::Service` \(`myService`\) resources that are specified in the same template\.

#### JSON<a name="quickref-autoscaling-example-9.json"></a>

```
{
  "Resources" : {
    "ECSScalableTarget" : {
      "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties" : {
        "MaxCapacity" : "6",
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
      MaxCapacity: 6
      MinCapacity: 1  
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

### Declaring a scaling policy for an Amazon ECS service \(metric: average request count per target\)<a name="w2ab1c23c21c15c33c17"></a>

The following example applies a target tracking scaling policy with the `ALBRequestCountPerTarget` predefined metric to an ECS service\. The policy is used to add capacity to the ECS service when the request count per target \(per minute\) exceeds the target value\. Because the value of `DisableScaleIn` is set to `true`, the target tracking policy won't remove capacity from the scalable target\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html) intrinsic functions to construct the `ResourceLabel` property with the logical names of the `AWS::ElasticLoadBalancingV2::LoadBalancer` \(`myLoadBalancer`\) and `AWS::ElasticLoadBalancingV2::TargetGroup` \(`myTargetGroup`\) resources that are specified in the same template\.

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

### Declaring a scheduled action with a cron expression for a Lambda function<a name="w2ab1c23c21c15c33c19"></a>

This snippet registers the provisioned concurrency for a function alias \([AWS::Lambda::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-alias.html)\) named `BLUE` using the [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource\. It also creates a scheduled action with a recurring schedule using a cron expression\. The time zone for the recurring schedule is UTC\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions in the `RoleARN` property to specify the ARN of the service\-linked role\. It uses the [Fn::Sub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html) intrinsic function to construct the `ResourceId` property with the logical name of the `AWS::Lambda::Function` or `AWS::Serverless::Function` resource that is specified in the same template\.

**Note**  
You can't allocate provisioned concurrency on an alias that points to the unpublished version \($LATEST\)\.  
For more information about how to create an AWS CloudFormation template for Lambda resources, see the blog post [Scheduling AWS Lambda Provisioned Concurrency for recurring peak usage](http://aws.amazon.com/blogs/compute/scheduling-aws-lambda-provisioned-concurrency-for-recurring-peak-usage/) on the AWS Compute Blog\.

#### JSON<a name="quickref-autoscaling-example-11.json"></a>

```
{
  "ScalableTarget" : {
    "Type" : "AWS::ApplicationAutoScaling::ScalableTarget",
    "Properties" : {
      "MaxCapacity" : 250,
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
          "ScalableTargetAction" : {
            "MinCapacity" : "250"
          },
          "ScheduledActionName" : "my-scale-out-scheduled-action",
          "Schedule" : "cron(0 18 * * ? *)",
          "EndTime" : "2022-12-31T12:00:00.000Z"
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
    MaxCapacity: 250
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
      - ScalableTargetAction:
          MinCapacity: 250
        ScheduledActionName: my-scale-out-scheduled-action
        Schedule: 'cron(0 18 * * ? *)'
        EndTime: '2022-12-31T12:00:00.000Z'
```

### Declaring a scheduled action with an `at` expression for a Spot Fleet<a name="w2ab1c23c21c15c33c21"></a>

This snippet shows how to create two scheduled actions that occur only once for an [AWS::EC2::SpotFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-spotfleet.html) resource using the [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) resource\. The time zone for each one\-time scheduled action is UTC\.

It uses the [Fn::Join](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-join.html) and [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html) intrinsic functions to construct the `ResourceId` property with the logical name of the `AWS::EC2::SpotFleet` resource that is specified in the same template\.

**Note**  
The Spot Fleet request must have a request type of `maintain`\. Automatic scaling isn't supported for one\-time requests or Spot blocks\.

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
            "ScalableTargetAction" : {
              "MaxCapacity" : "10",
              "MinCapacity" : "10"
            },
            "ScheduledActionName" : "my-scale-out-scheduled-action",
            "Schedule" : "at(2022-05-20T13:00:00)"
          },
          {
            "ScalableTargetAction" : {
              "MaxCapacity" : "0",
              "MinCapacity" : "0"
            },
            "ScheduledActionName" : "my-scale-in-scheduled-action",
            "Schedule" : "at(2022-05-20T21:00:00)"
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
        - ScalableTargetAction:
            MaxCapacity: 10
            MinCapacity: 10
          ScheduledActionName: my-scale-out-scheduled-action
          Schedule: 'at(2022-05-20T13:00:00)'
        - ScalableTargetAction:
            MaxCapacity: 0
            MinCapacity: 0
          ScheduledActionName: my-scale-in-scheduled-action
          Schedule: 'at(2022-05-20T21:00:00)'
```