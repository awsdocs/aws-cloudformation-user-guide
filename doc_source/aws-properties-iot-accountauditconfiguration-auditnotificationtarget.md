# AWS::IoT::AccountAuditConfiguration AuditNotificationTarget<a name="aws-properties-iot-accountauditconfiguration-auditnotificationtarget"></a>

Information about the targets to which audit notifications are sent\.

## Syntax<a name="aws-properties-iot-accountauditconfiguration-auditnotificationtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-accountauditconfiguration-auditnotificationtarget-syntax.json"></a>

```
{
  "[Enabled](#cfn-iot-accountauditconfiguration-auditnotificationtarget-enabled)" : Boolean,
  "[RoleArn](#cfn-iot-accountauditconfiguration-auditnotificationtarget-rolearn)" : String,
  "[TargetArn](#cfn-iot-accountauditconfiguration-auditnotificationtarget-targetarn)" : String
}
```

### YAML<a name="aws-properties-iot-accountauditconfiguration-auditnotificationtarget-syntax.yaml"></a>

```
  [Enabled](#cfn-iot-accountauditconfiguration-auditnotificationtarget-enabled): Boolean
  [RoleArn](#cfn-iot-accountauditconfiguration-auditnotificationtarget-rolearn): String
  [TargetArn](#cfn-iot-accountauditconfiguration-auditnotificationtarget-targetarn): String
```

## Properties<a name="aws-properties-iot-accountauditconfiguration-auditnotificationtarget-properties"></a>

`Enabled`  <a name="cfn-iot-accountauditconfiguration-auditnotificationtarget-enabled"></a>
True if notifications to the target are enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-accountauditconfiguration-auditnotificationtarget-rolearn"></a>
The ARN of the role that grants permission to send notifications to the target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-iot-accountauditconfiguration-auditnotificationtarget-targetarn"></a>
The ARN of the target \(SNS topic\) to which audit notifications are sent\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)