# AWS::AutoScaling::LifecycleHook<a name="aws-resource-as-lifecyclehook"></a>

Controls the state of an instance in an Auto Scaling group after it is launched or terminated\. When you use a lifecycle hook, the Auto Scaling group either pauses the instance after it is launched \(before it is put into service\) or pauses the instance as it is terminated \(before it is fully terminated\)\. For more information, see [Amazon EC2 Auto Scaling Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html) in the *Amazon EC2 Auto Scaling User Guide*\.

**Topics**
+ [Syntax](#aws-resource-autoscaling-lifecyclehook-syntax)
+ [Properties](#w3ab2c21c10d139b9)
+ [Return Value](#w3ab2c21c10d139c11)
+ [Example](#w3ab2c21c10d139c13)
+ [See Also](#aws-resource-autoscaling-lifecyclehook-seealso)

## Syntax<a name="aws-resource-autoscaling-lifecyclehook-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-autoscaling-lifecyclehook-syntax.json"></a>

```
{
  "Type" : "AWS::AutoScaling::LifecycleHook",
  "Properties" : {
    "[AutoScalingGroupName](#cfn-as-lifecyclehook-autoscalinggroupname)" : String,
    "[DefaultResult](#cfn-as-lifecyclehook-defaultresult)" : String,
    "[HeartbeatTimeout](#cfn-as-lifecyclehook-heartbeattimeout)" : Integer,
    "[LifecycleHookName](#cfn-as-lifecyclehook-lifecyclehookname)" : String,
    "[LifecycleTransition](#cfn-as-lifecyclehook-lifecycletransition)" : String,
    "[NotificationMetadata](#cfn-as-lifecyclehook-notificationmetadata)" : String,
    "[NotificationTargetARN](#cfn-as-lifecyclehook-notificationtargetarn)" : String,
    "[RoleARN](#cfn-as-lifecyclehook-rolearn)" : String
  }
}
```

### YAML<a name="aws-resource-autoscaling-lifecyclehook-syntax.yaml"></a>

```
Type: "AWS::AutoScaling::LifecycleHook"
Properties:
  [AutoScalingGroupName](#cfn-as-lifecyclehook-autoscalinggroupname): String
  [DefaultResult](#cfn-as-lifecyclehook-defaultresult): String
  [HeartbeatTimeout](#cfn-as-lifecyclehook-heartbeattimeout): Integer
  [LifecycleHookName](#cfn-as-lifecyclehook-lifecyclehookname): String
  [LifecycleTransition](#cfn-as-lifecyclehook-lifecycletransition): String
  [NotificationMetadata](#cfn-as-lifecyclehook-notificationmetadata): String
  [NotificationTargetARN](#cfn-as-lifecyclehook-notificationtargetarn): String
  [RoleARN](#cfn-as-lifecyclehook-rolearn): String
```

## Properties<a name="w3ab2c21c10d139b9"></a>

For information about valid and default values, see [LifecycleHook](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_LifecycleHook.html) in the *Amazon EC2 Auto Scaling API Reference*\.

`AutoScalingGroupName`  <a name="cfn-as-lifecyclehook-autoscalinggroupname"></a>
The name of the Auto Scaling group for the lifecycle hook\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DefaultResult`  <a name="cfn-as-lifecyclehook-defaultresult"></a>
The action the Auto Scaling group takes when the lifecycle hook timeout elapses or if an unexpected failure occurs\. Valid values are `CONTINUE` \(default\) and `ABANDON`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HeartbeatTimeout`  <a name="cfn-as-lifecyclehook-heartbeattimeout"></a>
The amount of time that can elapse before the lifecycle hook times out\. When the lifecycle hook times out, Auto Scaling performs the action that you specified in the DefaultResult property\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LifecycleHookName`  <a name="cfn-as-lifecyclehook-lifecyclehookname"></a>
The name of the lifecycle hook\. Length Constraints: Minimum length of 1\. Maximum length of 255\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LifecycleTransition`  <a name="cfn-as-lifecyclehook-lifecycletransition"></a>
The state of the Amazon EC2 instance to which you want to attach the lifecycle hook\. For valid values, see the `LifecycleTransition` content for the [LifecycleHook](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_LifecycleHook.html) data type in the *Amazon EC2 Auto Scaling API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NotificationMetadata`  <a name="cfn-as-lifecyclehook-notificationmetadata"></a>
Additional information that you want to include when Auto Scaling sends a message to the notification target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NotificationTargetARN`  <a name="cfn-as-lifecyclehook-notificationtargetarn"></a>
The Amazon resource name \(ARN\) of the notification target that Auto Scaling uses to notify you when an instance is in the transition state for the lifecycle hook\. You can specify an Amazon SQS queue or an Amazon SNS topic\. The notification message includes the following information: lifecycle action token, user account ID, Auto Scaling group name, lifecycle hook name, instance ID, lifecycle transition, and notification metadata\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RoleARN`  <a name="cfn-as-lifecyclehook-rolearn"></a>
The ARN of the IAM role that allows the Auto Scaling group to publish to the specified notification target\. The role requires permissions to Amazon SNS and Amazon SQS\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d139c11"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myLifecycleHook" }
```

`Ref` returns the lifecycle hook name, such as `mylifecyclehookname`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d139c13"></a>

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
+  [LifecycleHook](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_LifecycleHook.html) in the *Amazon EC2 Auto Scaling API Reference* \(for valid values and default values\) 
+  [Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html) in the *Amazon EC2 Auto Scaling User Guide* 