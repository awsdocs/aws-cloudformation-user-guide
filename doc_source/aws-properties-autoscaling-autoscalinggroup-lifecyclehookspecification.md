# AWS::AutoScaling::AutoScalingGroup LifecycleHookSpecification<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification"></a>

 `LifecycleHookSpecification` specifies a list of lifecycle hooks for the `LifecycleHookSpecificationList` property of [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)\. `LifecycleHookSpecification` defines lifecycle hooks for an Auto Scaling group that specify actions to perform when Amazon EC2 Auto Scaling launches or terminates instances\. 

For more information, see [Amazon EC2 Auto Scaling lifecycle hooks](https://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html) in the *Amazon EC2 Auto Scaling User Guide*\. You can find a sample template snippet in the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-as-lifecyclehook.html#aws-resource-as-lifecyclehook--examples) section of the `AWS::AutoScaling::LifecycleHook` documentation\.

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-syntax.json"></a>

```
{
  "[DefaultResult](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-defaultresult)" : String,
  "[HeartbeatTimeout](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-heartbeattimeout)" : Integer,
  "[LifecycleHookName](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecyclehookname)" : String,
  "[LifecycleTransition](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecycletransition)" : String,
  "[NotificationMetadata](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationmetadata)" : String,
  "[NotificationTargetARN](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationtargetarn)" : String,
  "[RoleARN](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-rolearn)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-syntax.yaml"></a>

```
  [DefaultResult](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-defaultresult): String
  [HeartbeatTimeout](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-heartbeattimeout): Integer
  [LifecycleHookName](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecyclehookname): String
  [LifecycleTransition](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecycletransition): String
  [NotificationMetadata](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationmetadata): String
  [NotificationTargetARN](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationtargetarn): String
  [RoleARN](#cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-rolearn): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-lifecyclehookspecification-properties"></a>

`DefaultResult`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-defaultresult"></a>
The action the Auto Scaling group takes when the lifecycle hook timeout elapses or if an unexpected failure occurs\. The valid values are `CONTINUE` and `ABANDON` \(default\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeartbeatTimeout`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-heartbeattimeout"></a>
The maximum time, in seconds, that can elapse before the lifecycle hook times out\. If the lifecycle hook times out, Amazon EC2 Auto Scaling performs the default action\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecycleHookName`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecyclehookname"></a>
The name of the lifecycle hook\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[A-Za-z0-9\-_\/]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecycleTransition`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-lifecycletransition"></a>
The state of the EC2 instance to attach the lifecycle hook to\. The valid values are:  
+ autoscaling:EC2\_INSTANCE\_LAUNCHING
+ autoscaling:EC2\_INSTANCE\_TERMINATING
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationMetadata`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationmetadata"></a>
Additional information that you want to include any time Amazon EC2 Auto Scaling sends a message to the notification target\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1023`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationTargetARN`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-notificationtargetarn"></a>
The Amazon Resource Name \(ARN\) of the notification target that Amazon EC2 Auto Scaling uses to notify you when an instance is in the transition state for the lifecycle hook\. You can specify an Amazon SQS queue or an Amazon SNS topic\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleARN`  <a name="cfn-autoscaling-autoscalinggroup-lifecyclehookspecification-rolearn"></a>
The ARN of the IAM role that allows the Auto Scaling group to publish to the specified notification target, for example, an Amazon SNS topic or an Amazon SQS queue\. For information about creating this role, see [Preparing for notifications](https://docs.aws.amazon.com/autoscaling/ec2/userguide/lifecycle-hooks.html#preparing-for-notification) in the *Amazon EC2 Auto Scaling User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)