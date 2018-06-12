# AWS Systems Manager MaintenanceWindowTask NotificationConfig<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig"></a>

<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-description"></a>The `NotificationConfig` property type specifies configurations for sending notifications for a Maintenance Window task in AWS Systems Manager\.

<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-inheritance"></a> `NotificationConfig` is a property of the [Systems Manager MaintenanceWindowTask MaintenanceWindowRunCommandParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters.md) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-syntax.json"></a>

```
{
  "[NotificationArn](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationarn)" : String,
  "[NotificationType](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationtype)" : String,
  "[NotificationEvents](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationevents)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-syntax.yaml"></a>

```
[NotificationArn](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationarn): String
[NotificationType](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationtype): String
[NotificationEvents](#cfn-ssm-maintenancewindowtask-notificationconfig-notificationevents): 
  - String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-notificationconfig-properties"></a>

`NotificationArn`  <a name="cfn-ssm-maintenancewindowtask-notificationconfig-notificationarn"></a>
An Amazon Resource Name \(ARN\) for an Amazon SNS topic\. Run Command pushes notifications about command status changes to this topic\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NotificationType`  <a name="cfn-ssm-maintenancewindowtask-notificationconfig-notificationtype"></a>
The notification type\.  
+ `Command`: Receive notification when the status of a command changes\.
+ `Invocation`: For commands sent to multiple instances, receive notification on a per\-instance basis when the status of a command changes\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`NotificationEvents`  <a name="cfn-ssm-maintenancewindowtask-notificationconfig-notificationevents"></a>
The different events that you can receive notifications for\. These events include the following: `All` \(events\), `InProgress`, `Success`, `TimedOut`, `Cancelled`, `Failed`\. To learn more about these events, see [Understanding Command Statuses](http://docs.aws.amazon.com/systems-manager/latest/userguide/monitor-commands.html) in the *AWS Systems Manager User Guide*\.  
 *Required*: No  
 *Type*: List of strings  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 