# AWS::AutoScaling::LifecycleHook<a name="aws-resource-as-lifecyclehook"></a>

The `AWS::AutoScaling::LifecycleHook` resource specifies lifecycle hooks for an Auto Scaling group\. These hooks enable an Auto Scaling group to be aware of events in the Auto Scaling instance lifecycle, and then perform a custom action when the corresponding lifecycle event occurs\. A lifecycle hook provides a specified amount of time \(one hour by default\) to complete the lifecycle action before the instance transitions to the next state\. 

There are two types of lifecycle hooks that can be implemented: launch lifecycle hooks and termination lifecycle hooks\. Use a launch lifecycle hook to prepare instances for use or to delay instances from registering behind the load balancer before their configuration has been applied completely\. Use a termination lifecycle hook to prepare running instances to be shut down\. 

For more information, see [Amazon EC2 Auto Scaling lifecycle hooks](https://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html) in the *Amazon EC2 Auto Scaling User Guide* and [PutLifecycleHook](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PutLifecycleHook.html) in the *Amazon EC2 Auto Scaling API Reference*\.

## Syntax<a name="aws-resource-as-lifecyclehook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-as-lifecyclehook-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::LifecycleHook",
  "Properties" : {
      "[AutoScalingGroupName](#cfn-as-lifecyclehook-autoscalinggroupname)" : String,
      "[DefaultResult](#cfn-as-lifecyclehook-defaultresult)" : String,
      "[HeartbeatTimeout](#cfn-as-lifecyclehook-heartbeattimeout)" : Integer,
      "[LifecycleHookName](#cfn-autoscaling-lifecyclehook-lifecyclehookname)" : String,
      "[LifecycleTransition](#cfn-as-lifecyclehook-lifecycletransition)" : String,
      "[NotificationMetadata](#cfn-as-lifecyclehook-notificationmetadata)" : String,
      "[NotificationTargetARN](#cfn-as-lifecyclehook-notificationtargetarn)" : String,
      "[RoleARN](#cfn-as-lifecyclehook-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-as-lifecyclehook-syntax.yaml"></a>

```
Type: AWS::AutoScaling::LifecycleHook
Properties: 
  [AutoScalingGroupName](#cfn-as-lifecyclehook-autoscalinggroupname): String
  [DefaultResult](#cfn-as-lifecyclehook-defaultresult): String
  [HeartbeatTimeout](#cfn-as-lifecyclehook-heartbeattimeout): Integer
  [LifecycleHookName](#cfn-autoscaling-lifecyclehook-lifecyclehookname): String
  [LifecycleTransition](#cfn-as-lifecyclehook-lifecycletransition): String
  [NotificationMetadata](#cfn-as-lifecyclehook-notificationmetadata): String
  [NotificationTargetARN](#cfn-as-lifecyclehook-notificationtargetarn): String
  [RoleARN](#cfn-as-lifecyclehook-rolearn): String
```

## Properties<a name="aws-resource-as-lifecyclehook-properties"></a>

`AutoScalingGroupName`  <a name="cfn-as-lifecyclehook-autoscalinggroupname"></a>
The name of the Auto Scaling group for the lifecycle hook\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DefaultResult`  <a name="cfn-as-lifecyclehook-defaultresult"></a>
The action the Auto Scaling group takes when the lifecycle hook timeout elapses or if an unexpected failure occurs\. The valid values are `CONTINUE` and `ABANDON` \(default\)\.  
For more information, see [Adding lifecycle hooks](https://docs.aws.amazon.com/autoscaling/ec2/userguide/adding-lifecycle-hooks.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeartbeatTimeout`  <a name="cfn-as-lifecyclehook-heartbeattimeout"></a>
The maximum time, in seconds, that can elapse before the lifecycle hook times out\. The range is from `30` to `7200` seconds\. The default value is `3600` seconds \(1 hour\)\. If the lifecycle hook times out, Amazon EC2 Auto Scaling performs the action that you specified in the `DefaultResult` property\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecycleHookName`  <a name="cfn-autoscaling-lifecyclehook-lifecyclehookname"></a>
The name of the lifecycle hook\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[A-Za-z0-9\-_\/]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LifecycleTransition`  <a name="cfn-as-lifecyclehook-lifecycletransition"></a>
The instance state to which you want to attach the lifecycle hook\. The valid values are:  
+ autoscaling:EC2\_INSTANCE\_LAUNCHING
+ autoscaling:EC2\_INSTANCE\_TERMINATING
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationMetadata`  <a name="cfn-as-lifecyclehook-notificationmetadata"></a>
Additional information that is included any time Amazon EC2 Auto Scaling sends a message to the notification target\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1023`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationTargetARN`  <a name="cfn-as-lifecyclehook-notificationtargetarn"></a>
The Amazon Resource Name \(ARN\) of the notification target that Amazon EC2 Auto Scaling uses to notify you when an instance is in the transition state for the lifecycle hook\. You can specify an Amazon SQS queue or an Amazon SNS topic\. The notification message includes the following information: lifecycle action token, user account ID, Auto Scaling group name, lifecycle hook name, instance ID, lifecycle transition, and notification metadata\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-as-lifecyclehook-rolearn"></a>
The ARN of the IAM role that allows the Auto Scaling group to publish to the specified notification target, for example, an Amazon SNS topic or an Amazon SQS queue\. For information about creating this role, see [Configuring a notification target for a lifecycle hook](https://docs.aws.amazon.com/autoscaling/ec2/userguide/configuring-lifecycle-hook-notifications.html) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-as-lifecyclehook-return-values"></a>

### Ref<a name="aws-resource-as-lifecyclehook-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mylifecyclehook`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-as-lifecyclehook--examples"></a>

The following examples specify lifecycle hooks\. 

For examples of CloudFormation stack templates with lifecycle hooks, see our [GitHub repository](https://github.com/aws-samples/amazon-ec2-auto-scaling-group-examples)\. Included are examples of launch lifecycle hooks that work with a user data script that is defined in the Auto Scaling group's launch template\.

### Lifecycle hook for instance termination<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_termination"></a>

The following example specifies a lifecycle hook that supports a custom action at instance termination\. It uses the `Ref` intrinsic function to refer to an Auto Scaling group \(whose logical name is `myASG`\) that is declared elsewhere in the same template\. It uses the `NotificationMetadata` property to specify additional information to be sent with the notification, such as the name of the cluster to which the instance belongs\.

This snippet does not include the Lambda/EventBridge rule resources that would need to exist or be created to complete the configuration\. For information about creating these resources, see [Configuring a notification target for a lifecycle hook](https://docs.aws.amazon.com/autoscaling/ec2/userguide/configuring-lifecycle-hook-notifications.html) in the *Amazon EC2 Auto Scaling User Guide*\.

#### JSON<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_termination--json"></a>

```
{
  "myTerminationLifecycleHook":{
    "Type":"AWS::AutoScaling::LifecycleHook",
    "Properties":{
      "AutoScalingGroupName":{
        "Ref":"myASG"
      },
      "LifecycleTransition":"autoscaling:EC2_INSTANCE_TERMINATING",
      "HeartbeatTimeout": 300,
      "DefaultResult": "CONTINUE",
      "NotificationMetadata": "optional metadata"
    }
  }
}
```

#### YAML<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_termination--yaml"></a>

```
---
myTerminationLifecycleHook: 
  Type: AWS::AutoScaling::LifecycleHook
  Properties: 
    AutoScalingGroupName: 
      Ref: myASG
    LifecycleTransition: "autoscaling:EC2_INSTANCE_TERMINATING"
    HeartbeatTimeout: 300
    DefaultResult: "CONTINUE"
    NotificationMetadata: "optional metadata"
```

### Lifecycle hook for instance launch<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_launch"></a>

The following example specifies a lifecycle hook that supports a custom action at instance launch\. The lifecycle hook is added to a new Auto Scaling group that's created from the same snippet\.

This example solution uses the `NotificationTargetARN` and `RoleARN` properties to specify the Amazon SQS queue and IAM role to use to receive notification when a lifecycle action occurs\. This snippet does not include the Amazon SQS queue and IAM role resources that would need to exist or be created to complete the configuration\. For information about creating these resources, see [Configuring a notification target for a lifecycle hook](https://docs.aws.amazon.com/autoscaling/ec2/userguide/configuring-lifecycle-hook-notifications.html) in the *Amazon EC2 Auto Scaling User Guide*\.

#### JSON<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_launch--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Parameters":{
    "Subnets":{
      "Type":"CommaDelimitedList"
    }
  },
  "Resources":{
    "myASG":{
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "DesiredCapacity":"2",
        "MaxSize":"3",
        "MinSize":"1",
        "LaunchTemplate": {
          "LaunchTemplateId": {
            "Ref":"myLaunchTemplate"
          },
          "Version":{
            "Ref":"myLaunchTemplateVersionNumber"
          }
        },
        "VPCZoneIdentifier":{
          "Ref":"Subnets"
        },
        "LifecycleHookSpecificationList":[
          {
            "LifecycleTransition":"autoscaling:EC2_INSTANCE_LAUNCHING",
            "LifecycleHookName":"myLaunchLifecycleHook",
            "HeartbeatTimeout":4800,
            "NotificationTargetARN":{
              "Fn::GetAtt":[
                "SQS",
                "Arn"
              ]
            },
            "RoleArn":{
              "Fn::Join":[
                ":",
                [
                  "arn:aws:iam:",
                  {
                    "Ref":"AWS::AccountId"
                  },
                  "role/role-name"
                ]
              ]
            }
          }
        ]
      }
    },
    "SQS":{
      "Type":"AWS::SQS::Queue"
    }
  }
}
```

#### YAML<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_launch--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  Subnets:
    Type: CommaDelimitedList
  AZs:
    Type: CommaDelimitedList
Resources:
  myASG:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      DesiredCapacity: '2'
      MaxSize: '3'
      MinSize: '1'
      LaunchTemplate:
        LaunchTemplateId: !Ref myLaunchTemplate
        Version: !Ref myLaunchTemplateVersionNumber
      VPCZoneIdentifier: !Ref Subnets
      LifecycleHookSpecificationList:
        - LifecycleTransition: "autoscaling:EC2_INSTANCE_LAUNCHING"
          LifecycleHookName: "myLaunchLifecycleHook"
          HeartbeatTimeout: 4800
          NotificationTargetARN: !GetAtt SQS.Arn
          RoleARN: !Join 
            - ':'
            - - 'arn:aws:iam:'
              - !Ref 'AWS::AccountId'
              - role/role-name
  SQS:
    Type: AWS::SQS::Queue
```