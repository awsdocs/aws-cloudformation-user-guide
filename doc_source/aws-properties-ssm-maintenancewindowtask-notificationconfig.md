# AWS::SSM::MaintenanceWindowTask NotificationConfig<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig"></a>

The `NotificationConfig` property type specifies configurations for sending notifications for a maintenance window task in AWS Systems Manager\.

 `NotificationConfig` is a property of the [MaintenanceWindowRunCommandParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters.html) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-syntax.json"></a>

```
{
  "[NotificationArn](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationarn)" : String,
  "[NotificationEvents](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationevents)" : [ String, ... ],
  "[NotificationType](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationtype)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-syntax.yaml"></a>

```
  [NotificationArn](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationarn): String
  [NotificationEvents](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationevents): 
    - String
  [NotificationType](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationtype): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-properties"></a>

`NotificationArn`  <a name="cfn-ssm-maintenancewindowtask-notificationconfig-notificationarn"></a>
An Amazon Resource Name \(ARN\) for an Amazon Simple Notification Service \(Amazon SNS\) topic\. Run Command pushes notifications about command status changes to this topic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationEvents`  <a name="cfn-ssm-maintenancewindowtask-notificationconfig-notificationevents"></a>
The different events that you can receive notifications for\. These events include the following: `All` \(events\), `InProgress`, `Success`, `TimedOut`, `Cancelled`, `Failed`\. To learn more about these events, see [Configuring Amazon SNS Notifications for AWS Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/monitoring-sns-notifications.html) in the *AWS Systems Manager User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationType`  <a name="cfn-ssm-maintenancewindowtask-notificationconfig-notificationtype"></a>
The notification type\.  
+  `Command`: Receive notification when the status of a command changes\.
+  `Invocation`: For commands sent to multiple instances, receive notification on a per\-instance basis when the status of a command changes\.
*Required*: No  
*Type*: String  
*Allowed values*: `Command | Invocation`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)