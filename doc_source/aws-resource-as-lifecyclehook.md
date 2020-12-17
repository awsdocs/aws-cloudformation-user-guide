# AWS::AutoScaling::LifecycleHook<a name="aws-resource-as-lifecyclehook"></a>

The AWS::AutoScaling::LifecycleHook resource specifies lifecycle hooks for an Auto Scaling group\. Lifecycle hooks specify actions to perform when Amazon EC2 Auto Scaling launches or terminates instances\. When you use a lifecycle hook, the Auto Scaling group pauses the instance either after it is launched \(before it is put into service\) or as it is terminated \(before it is fully terminated\)\. 

For more information, see [PutLifecycleHook](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_PutLifecycleHook.html) in the *Amazon EC2 Auto Scaling API Reference* and [Amazon EC2 Auto Scaling lifecycle hooks](https://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html) in the *Amazon EC2 Auto Scaling User Guide*\.

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
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeartbeatTimeout`  <a name="cfn-as-lifecyclehook-heartbeattimeout"></a>
The amount of time, in seconds, that can elapse before the lifecycle hook times out\. If the lifecycle hook times out, Amazon EC2 Auto Scaling performs the action that you specified in the `DefaultResult` property\.  
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
The ARN of the IAM role that allows the Auto Scaling group to publish to the specified notification target, for example, an Amazon SNS topic or an Amazon SQS queue\. For information about creating this role, see [Preparing for notifications](https://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html#preparing-for-notification) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-as-lifecyclehook-return-values"></a>

### Ref<a name="aws-resource-as-lifecyclehook-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example: `mylifecyclehook`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

## Examples<a name="aws-resource-as-lifecyclehook--examples"></a>

The following examples specify lifecycle hooks\.

### Lifecycle hook for instance termination<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_termination"></a>

The following example specifies a lifecycle hook that supports a custom action at instance termination\. It uses the `Ref` intrinsic function to refer to an Auto Scaling group \(whose logical name is `myASG`\) that is declared elsewhere in the same template\.

Note that the snippet uses the `NotificationTargetARN` and `RoleARN` properties to specify the Amazon SNS topic and IAM role to use to receive notification when a lifecycle action occurs\.

#### JSON<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_termination--json"></a>

```
{
  "myLifecycleHook":{
    "Type":"AWS::AutoScaling::LifecycleHook",
    "Properties":{
      "AutoScalingGroupName":{
        "Ref":"myASG"
      },
      "LifecycleTransition":"autoscaling:EC2_INSTANCE_TERMINATING",
      "NotificationTargetARN":{
        "Ref":"lifecycleHookTopic"
      },
      "RoleARN":{
        "Fn::GetAtt":[
          "lifecycleHookRole",
          "Arn"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_termination--yaml"></a>

```
---
myLifecycleHook: 
  Type: AWS::AutoScaling::LifecycleHook
  Properties: 
    AutoScalingGroupName: 
      Ref: myASG
    LifecycleTransition: "autoscaling:EC2_INSTANCE_TERMINATING"
    NotificationTargetARN: 
      Ref: lifecycleHookTopic
    RoleARN: 
      Fn::GetAtt: 
        - lifecycleHookRole
        - Arn
```

### Lifecycle hook for instance launch<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_launch"></a>

The following example specifies a lifecycle hook that supports a custom action at instance launch\. The lifecycle hook is added to a new Auto Scaling group that's created from the same snippet\. For more information, see [LifecycleHookSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification.html)\. 

Note that the snippet uses the `NotificationTargetARN` and `RoleARN` properties to specify the Amazon SQS queue and IAM role to use to receive notification when a lifecycle action occurs\.

#### JSON<a name="aws-resource-as-lifecyclehook--examples--Lifecycle_hook_for_instance_launch--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Parameters":{
    "Subnets":{
      "Type":"CommaDelimitedList"
    },
    "AZs":{
      "Type":"CommaDelimitedList"
    }
  },
  "Resources":{
    "myASG":{
      "Type":"AWS::AutoScaling::AutoScalingGroup",
      "Properties":{
        "AvailabilityZones":[
          {
            "Ref":"AZs"
          }
        ],
        "VPCZoneIdentifier":{
          "Ref":"Subnets"
        },
        "DesiredCapacity":"2",
        "MaxSize":"3",
        "MinSize":"1",
        "LaunchConfigurationName":{
          "Ref":"myLaunchConfig"
        },
        "LifecycleHookSpecificationList":[
          {
            "LifecycleTransition":"autoscaling:EC2_INSTANCE_LAUNCHING",
            "LifecycleHookName":"myLifecycleHook",
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
      AvailabilityZones:
        - !Ref AZs
      VPCZoneIdentifier: !Ref Subnets
      DesiredCapacity: '2'
      MaxSize: '3'
      MinSize: '1'
      LaunchConfigurationName: !Ref myLaunchConfig
      LifecycleHookSpecificationList:
        - LifecycleTransition: "autoscaling:EC2_INSTANCE_LAUNCHING"
          LifecycleHookName: "myLifecycleHook"
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