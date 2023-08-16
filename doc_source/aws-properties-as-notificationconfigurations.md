# AWS::AutoScaling::AutoScalingGroup NotificationConfiguration<a name="aws-properties-as-notificationconfigurations"></a>

A structure that specifies an Amazon SNS notification configuration for the `NotificationConfigurations` property of the [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource\.

For an example template snippet, see [Auto scaling template snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-autoscaling.html)\.

For more information, see [Get Amazon SNS notifications when your Auto Scaling group scales](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ASGettingNotifications.html) in the *Amazon EC2 Auto Scaling User Guide*\.

## Syntax<a name="aws-properties-as-notificationconfigurations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-notificationconfigurations-syntax.json"></a>

```
{
  "[NotificationTypes](#cfn-as-group-notificationconfigurations-notificationtypes)" : [ String, ... ],
  "[TopicARN](#cfn-autoscaling-autoscalinggroup-notificationconfigurations-topicarn)" : String
}
```

### YAML<a name="aws-properties-as-notificationconfigurations-syntax.yaml"></a>

```
  [NotificationTypes](#cfn-as-group-notificationconfigurations-notificationtypes): 
    - String
  [TopicARN](#cfn-autoscaling-autoscalinggroup-notificationconfigurations-topicarn): String
```

## Properties<a name="aws-properties-as-notificationconfigurations-properties"></a>

`NotificationTypes`  <a name="cfn-as-group-notificationconfigurations-notificationtypes"></a>
A list of event types that send a notification\. Event types can include any of the following types\.   
*Allowed values*:  
+  `autoscaling:EC2_INSTANCE_LAUNCH` 
+  `autoscaling:EC2_INSTANCE_LAUNCH_ERROR` 
+  `autoscaling:EC2_INSTANCE_TERMINATE` 
+  `autoscaling:EC2_INSTANCE_TERMINATE_ERROR` 
+  `autoscaling:TEST_NOTIFICATION` 
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicARN`  <a name="cfn-autoscaling-autoscalinggroup-notificationconfigurations-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)