# Amazon EC2 Auto Scaling AutoScalingGroup NotificationConfiguration<a name="aws-properties-as-notificationconfigurations"></a>

The `NotificationConfiguration` property type specifies the events that the Auto Scaling group sends notifications for\.

The `NotificationConfigurations` property of the `[AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md)` resource contains a list of `NotificationConfiguration` property types\.

## Syntax<a name="w3ab2c21c14d109b7"></a>

### JSON<a name="aws-properties-as-notificationconfigurations-syntax.json"></a>

```
{
   "[NotificationTypes](#cfn-as-group-notificationconfigurations-notificationtypes)" : [ String, ... ],
   "[TopicARN](#cfn-as-group-notificationconfigurations-topicarn)" : String
}
```

### YAML<a name="aws-properties-as-notificationconfigurations-syntax.yaml"></a>

```
[NotificationTypes](#cfn-as-group-notificationconfigurations-notificationtypes):
  - String
[TopicARN](#cfn-as-group-notificationconfigurations-topicarn): String
```

## Properties<a name="w3ab2c21c14d109b9"></a>

`NotificationTypes`  <a name="cfn-as-group-notificationconfigurations-notificationtypes"></a>
A list of event types that trigger a notification\. Event types can include any of the following types: `autoscaling:EC2_INSTANCE_LAUNCH`, `autoscaling:EC2_INSTANCE_LAUNCH_ERROR`, `autoscaling:EC2_INSTANCE_TERMINATE`, `autoscaling:EC2_INSTANCE_TERMINATE_ERROR`, and `autoscaling:TEST_NOTIFICATION`\. For more information about event types, see [DescribeAutoScalingNotificationTypes](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_DescribeAutoScalingNotificationTypes.html) in the *Amazon EC2 Auto Scaling API Reference*\.  
*Required*: Yes  
*Type*: List of String values

`TopicARN`  <a name="cfn-as-group-notificationconfigurations-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service \(SNS\) topic\.  
*Required*: Yes  
*Type*: String

## Examples<a name="w3ab2c21c14d109c11"></a>

For NotificationConfigurations snippets, see [Auto Scaling Group with Notifications](quickref-autoscaling.md#scenario-as-notification)\.