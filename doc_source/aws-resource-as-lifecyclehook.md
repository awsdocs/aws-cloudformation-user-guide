# AWS::AutoScaling::LifecycleHook<a name="aws-resource-as-lifecyclehook"></a>

Use `AWS::AutoScaling::LifecycleHook` to control the state of an instance in an Auto Scaling group after it is launched or terminated\. When you use a lifecycle hook, the Auto Scaling group either pauses the instance after it is launched \(before it is put into service\) or pauses the instance as it is terminated \(before it is fully terminated\)\. For more information, see [Examples of How to Use Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html) in the *Auto Scaling User Guide*\.


+ [Syntax](#aws-resource-autoscaling-lifecyclehook-syntax)
+ [Properties](#w3ab2c21c10d117b9)
+ [Return Value](#w3ab2c21c10d117c11)
+ [Example](#w3ab2c21c10d117c13)
+ [See Also](#aws-resource-autoscaling-lifecyclehook-seealso)

## Syntax<a name="aws-resource-autoscaling-lifecyclehook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-lifecyclehook-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::LifecycleHook",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-autoscalinggroupname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-defaultresult)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-heartbeattimeout)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-lifecycletransition)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-notificationmetadata)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-notificationtargetarn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-rolearn)" : String
  }
}
```

### YAML<a name="aws-resource-autoscaling-lifecyclehook-syntax.yaml"></a>

```
Type: "AWS::AutoScaling::LifecycleHook"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-autoscalinggroupname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-defaultresult): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-heartbeattimeout): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-lifecycletransition): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-notificationmetadata): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-notificationtargetarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-as-lifecyclehook-rolearn): String
```

## Properties<a name="w3ab2c21c10d117b9"></a>

For information about valid and default values, see [LifecycleHook](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_LifecycleHook.html) in the *Auto Scaling API Reference*\.

`AutoScalingGroupName`  
The name of the Auto Scaling group for the lifecycle hook\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`DefaultResult`  
The action the Auto Scaling group takes when the lifecycle hook timeout elapses or if an unexpected failure occurs\. Valid values are `CONTINUE` \(default\) and `ABANDON`\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`HeartbeatTimeout`  
The amount of time that can elapse before the lifecycle hook times out\. When the lifecycle hook times out, Auto Scaling performs the action that you specified in the DefaultResult property\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`LifecycleTransition`  
The state of the Amazon EC2 instance to which you want to attach the lifecycle hook\. For valid values, see the `LifecycleTransition` content for the [LifecycleHook](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_LifecycleHook.html) data type in the *Auto Scaling API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`NotificationMetadata`  
Additional information that you want to include when Auto Scaling sends a message to the notification target\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`NotificationTargetARN`  
The Amazon resource name \(ARN\) of the notification target that Auto Scaling uses to notify you when an instance is in the transition state for the lifecycle hook\. You can specify an Amazon SQS queue or an Amazon SNS topic\. The notification message includes the following information: lifecycle action token, user account ID, Auto Scaling group name, lifecycle hook name, instance ID, lifecycle transition, and notification metadata\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`RoleARN`  
The ARN of the IAM role that allows the Auto Scaling group to publish to the specified notification target\. The role requires permissions to Amazon SNS and Amazon SQS\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

## Return Value<a name="w3ab2c21c10d117c11"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myLifecycleHook" }
```

`Ref` returns the lifecycle hook name, such as `mylifecyclehookname`\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d117c13"></a>

In the following template snippet, the Auto Scaling pauses instances before completely terminating them\. While in the pending state, you can, for example, connect to the instance and download logs or any other data before the instance is terminated\.

### JSON<a name="aws-resource-autoscaling-lifecyclehook-example.json"></a>

```
"myLifecycleHook": {
  "Type": "AWS::AutoScaling::LifecycleHook",
  "Properties": {
    "AutoScalingGroupName": { "Ref": "myAutoScalingGroup" },
    "LifecycleTransition": "autoscaling:EC2_INSTANCE_TERMINATING",
    "NotificationTargetARN": { "Ref": "lifecycleHookTopic" },
    "RoleARN": { "Fn::GetAtt": [ "lifecycleHookRole", "Arn" ] }
  }
}
```

### YAML<a name="aws-resource-autoscaling-lifecyclehook-example.yaml"></a>

```
myLifecycleHook: 
  Type: "AWS::AutoScaling::LifecycleHook"
  Properties: 
    AutoScalingGroupName: 
      Ref: myAutoScalingGroup
    LifecycleTransition: "autoscaling:EC2_INSTANCE_TERMINATING"
    NotificationTargetARN: 
      Ref: lifecycleHookTopic
    RoleARN: 
      Fn::GetAtt: 
        - lifecycleHookRole
        - Arn
```

## See Also<a name="aws-resource-autoscaling-lifecyclehook-seealso"></a>

+  [LifecycleHook](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_LifecycleHook.html) in the *Auto Scaling API Reference* \(for valid values and default values\) 

+  [Examples of How to Use Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html) in the *Auto Scaling User Guide* 