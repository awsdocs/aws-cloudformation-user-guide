# Auto Scaling AutoScalingGroup LifecycleHookSpecification<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification"></a>

<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-description"></a>The `LifecycleHookSpecification` property type defines lifecycle hooks for an Auto Scaling group, which specify actions to perform when Auto Scaling launches or terminates instances\. For more information, see [ Auto Scaling Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html) in the *Auto Scaling User Guide*\.

<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-inheritance"></a> The `LifecycleHookSpecificationList` property of the [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) resource contains a list of `LifecycleHookSpecification` property types\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-defaultresult)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-heartbeattimeout)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecyclehookname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecycletransition)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationmetadata)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationtargetarn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-rolearn)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-defaultresult): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-heartbeattimeout): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecyclehookname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecycletransition): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationmetadata): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationtargetarn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-rolearn): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-properties"></a>

For more information about each property, including constraints, see [PutLifecycleHook](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_PutLifecycleHook.html) in the *Auto Scaling API Reference*\.

`DefaultResult`  
The action that the Auto Scaling group should take when the lifecycle hook timeout elapses or if an unexpected failure occurs\.  
*Valid values*: `CONTINUE`, `ABANDON` \(default\)  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`HeartbeatTimeout`  
The maximum time, in seconds, that can elapse before the lifecycle hook times out\. If the lifecycle hook times out, Auto Scaling performs the default action\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: No interruption 

`LifecycleHookName`  
The name of the lifecycle hook\. For constraints, see [ PutLifecycleHook](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_PutLifecycleHook.html) in the *Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`LifecycleTransition`  
The state of the EC2 instance to attach the lifecycle hook to\. For a list of lifecycle hook types, see [ DescribeLifecycleHookTypes](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_DescribeLifecycleHookTypes.html) in the *Auto Scaling API Reference*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`NotificationMetadata`  
Additional information to include when Auto Scaling sends a message to the notification target\. For constraints, see [ PutLifecycleHook](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_PutLifecycleHook.html) in the *Auto Scaling API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`NotificationTargetARN`  
The Amazon Resource Name \(ARN\) of the target that Auto Scaling sends notifications to when an instance is in the transition state for the lifecycle hook\. The notification target can be either an Amazon SQS queue or an Amazon SNS topic\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`RoleARN`  
The ARN of the IAM role that allows the Auto Scaling group to publish to the specified notification target\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

## Examples<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-examples"></a>

### <a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-example1"></a>

The following snippet specifies a lifecycle hook for an `AWS::AutoScaling::AutoScalingGroup` resource\.

#### JSON<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-example1.json"></a>

```
{
  "Resources": {
    "ASG": {
      "Type": "AWS::AutoScaling::AutoScalingGroup",
      "Properties": {
        "AvailabilityZones": [
          {
            "Ref": "AZParameter"
          }
        ],
        "VPCZoneIdentifier": {
          "Ref": "Subnets"
        },
        "DesiredCapacity": "0",
        "MaxSize": "0",
        "MinSize": "0",
        "LaunchConfigurationName": {
          "Ref": "LC"
        },
        "LifecycleHookSpecificationList": [
          {
            "LifecycleTransition": "autoscaling: EC2_INSTANCE_LAUNCHING",
            "LifecycleHookName": "myFirstLifecycleHook",
            "HeartbeatTimeout": 4800,
            "NotificationTargetARN": {
              "Fn::GetAtt": [
                "SQS",
                "Arn"
              ]
            }
          }
        ]
      }
    },
    "SQS": {
      "Type": "AWS::SQS::Queue"
    }
  }
}
```

#### YAML<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-example1.yaml"></a>

```
Resources:
  ASG:
    Type: 'AWS::AutoScaling::AutoScalingGroup'
    Properties:
      AvailabilityZones:
        - !Ref AZParameter
      VPCZoneIdentifier: !Ref Subnets
      DesiredCapacity: '0'
      MaxSize: '0'
      MinSize: '0'
      LaunchConfigurationName: !Ref LC
      LifecycleHookSpecificationList:
        - LifecycleTransition: 'autoscaling:EC2_INSTANCE_LAUNCHING'
          LifecycleHookName: 'myFirstLifecycleHook'
          HeartbeatTimeout: 4800
          NotificationTargetARN: !GetAtt SQS.Arn
  SQS:
    Type: 'AWS::SQS::Queue'
```

## See Also<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-seealso"></a>

+ [ Auto Scaling Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html) in the *Auto Scaling User Guide*

+ [ PutLifecycleHook](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_PutLifecycleHook.html) in the *Auto Scaling API Reference*