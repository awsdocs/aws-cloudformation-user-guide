# AWS::IoT::AccountAuditConfiguration<a name="aws-resource-iot-accountauditconfiguration"></a>

Use the `AWS::IoT::AccountAuditConfiguration` resource to configure or reconfigure the Device Defender audit settings for your account\. Settings include how audit notifications are sent and which audit checks are enabled or disabled\. For API reference, see [UpdateAccountAuditConfiguration](https://docs.aws.amazon.com/iot/latest/apireference/API_UpdateAccountAuditConfiguration.html) and for detailed information on all available audit checks, see [Audit checks](https://docs.aws.amazon.com/iot/latest/developerguide/device-defender-audit-checks.html)\.

## Syntax<a name="aws-resource-iot-accountauditconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-accountauditconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::AccountAuditConfiguration",
  "Properties" : {
      "[AccountId](#cfn-iot-accountauditconfiguration-accountid)" : String,
      "[AuditCheckConfigurations](#cfn-iot-accountauditconfiguration-auditcheckconfigurations)" : AuditCheckConfigurations,
      "[AuditNotificationTargetConfigurations](#cfn-iot-accountauditconfiguration-auditnotificationtargetconfigurations)" : AuditNotificationTargetConfigurations,
      "[RoleArn](#cfn-iot-accountauditconfiguration-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-iot-accountauditconfiguration-syntax.yaml"></a>

```
Type: AWS::IoT::AccountAuditConfiguration
Properties: 
  [AccountId](#cfn-iot-accountauditconfiguration-accountid): String
  [AuditCheckConfigurations](#cfn-iot-accountauditconfiguration-auditcheckconfigurations): 
    AuditCheckConfigurations
  [AuditNotificationTargetConfigurations](#cfn-iot-accountauditconfiguration-auditnotificationtargetconfigurations): 
    AuditNotificationTargetConfigurations
  [RoleArn](#cfn-iot-accountauditconfiguration-rolearn): String
```

## Properties<a name="aws-resource-iot-accountauditconfiguration-properties"></a>

`AccountId`  <a name="cfn-iot-accountauditconfiguration-accountid"></a>
The ID of the account\. You can use the expression `!Sub "${AWS::AccountId}"` to use your account ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AuditCheckConfigurations`  <a name="cfn-iot-accountauditconfiguration-auditcheckconfigurations"></a>
Specifies which audit checks are enabled and disabled for this account\.  
Some data collection might start immediately when certain checks are enabled\. When a check is disabled, any data collected so far in relation to the check is deleted\. To disable a check, set the value of the `Enabled:` key to `false`\.  
If an enabled check is removed from the template, it will also be disabled\.  
You can't disable a check if it's used by any scheduled audit\. You must delete the check from the scheduled audit or delete the scheduled audit itself to disable the check\.  
For more information on avialbe auidt checks see [AWS::IoT::AccountAuditConfiguration AuditCheckConfigurations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iot-accountauditconfiguration-auditcheckconfigurations.html)  
*Required*: Yes  
*Type*: [AuditCheckConfigurations](aws-properties-iot-accountauditconfiguration-auditcheckconfigurations.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuditNotificationTargetConfigurations`  <a name="cfn-iot-accountauditconfiguration-auditnotificationtargetconfigurations"></a>
Information about the targets to which audit notifications are sent\.  
*Required*: No  
*Type*: [AuditNotificationTargetConfigurations](aws-properties-iot-accountauditconfiguration-auditnotificationtargetconfigurations.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-accountauditconfiguration-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role that grants permission to AWS IoT to access information about your devices, policies, certificates, and other items as required when performing an audit\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-accountauditconfiguration-return-values"></a>

### Ref<a name="aws-resource-iot-accountauditconfiguration-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the account ID\. 

## Examples<a name="aws-resource-iot-accountauditconfiguration--examples"></a>



### <a name="aws-resource-iot-accountauditconfiguration--examples--"></a>



#### JSON<a name="aws-resource-iot-accountauditconfiguration--examples----json"></a>

```
{ "AWSTemplateFormatVersion": "2010-09-09", "Description": "Amazon
            Web Services IoT AccountAuditConfiguration Sample Template", "Resources": {
            "MyAccountAuditConfiguration": { "Type": "AWS::IoT::AccountAuditConfiguration",
            "Properties": { "AccountId": "${AWS::AccountId}", "AuditCheckConfigurations": {
            "AuthenticatedCognitoRoleOverlyPermissiveCheck": { "Enabled": true },
            "CaCertificateExpiringCheck": { "Enabled": true }, "CaCertificateKeyQualityCheck": {
            "Enabled": true }, "ConflictingClientIdsCheck": { "Enabled": true },
            "DeviceCertificateExpiringCheck": { "Enabled": true },
            "DeviceCertificateKeyQualityCheck": { "Enabled": true }, "DeviceCertificateSharedCheck":
            { "Enabled": true }, "IotPolicyOverlyPermissiveCheck": { "Enabled": true },
            "IotRoleAliasAllowsAccessToUnusedServicesCheck": { "Enabled": true },
            "IotRoleAliasOverlyPermissiveCheck": { "Enabled": true }, "LoggingDisabledCheck": {
            "Enabled": true }, "RevokedCaCertificateStillActiveCheck": { "Enabled": true },
            "RevokedDeviceCertificateStillActiveCheck": { "Enabled": true },
            "UnauthenticatedCognitoRoleOverlyPermissiveCheck": { "Enabled": true } },
            "AuditNotificationTargetConfigurations": { "Sns": { "TargetArn":
            "arn:aws:sns:us-east-1:123456789012:AuditNotifications", "RoleArn":
            "arn:aws:iam::123456789012:role/RoleForIoTAuditNotifications", "Enabled": true } },
            "RoleArn": "arn:aws:iam::123456789012:role/service-role/AWSIoTDeviceDefenderAudit" } } }
            }
```

#### YAML<a name="aws-resource-iot-accountauditconfiguration--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09 Description: Amazon Web
            Services IoT AccountAuditConfiguration Sample Template Resources:
            MyAccountAuditConfiguration: Type: 'AWS::IoT::AccountAuditConfiguration' Properties:
            AccountId: !Sub '${AWS::AccountId}' AuditCheckConfigurations:
            AuthenticatedCognitoRoleOverlyPermissiveCheck: Enabled: True CaCertificateExpiringCheck:
            Enabled: True CaCertificateKeyQualityCheck: Enabled: True ConflictingClientIdsCheck:
            Enabled: True DeviceCertificateExpiringCheck: Enabled: True
            DeviceCertificateKeyQualityCheck: Enabled: True DeviceCertificateSharedCheck: Enabled:
            True IotPolicyOverlyPermissiveCheck: Enabled: True
            IotRoleAliasAllowsAccessToUnusedServicesCheck: Enabled: True
            IotRoleAliasOverlyPermissiveCheck: Enabled: True LoggingDisabledCheck: Enabled: True
            RevokedCaCertificateStillActiveCheck: Enabled: True
            RevokedDeviceCertificateStillActiveCheck: Enabled: True
            UnauthenticatedCognitoRoleOverlyPermissiveCheck: Enabled: True
            AuditNotificationTargetConfigurations: Sns: TargetArn:
            'arn:aws:sns:us-east-1:123456789012:AuditNotifications' RoleArn:
            'arn:aws:iam::123456789012:role/RoleForIoTAuditNotifications' Enabled: true RoleArn:
            'arn:aws:iam::123456789012:role/service-role/AWSIoTDeviceDefenderAudit'
```

## See also<a name="aws-resource-iot-accountauditconfiguration--seealso"></a>

When you use CloudFormation to perform drift detection for `AccountAuditConfiguration`, it won't compare values that aren't part of the stack template\. In `AccountAuditConfiguration`, specifying a configuration for every check is optional, and skipped checks are interpreted as disabled\. To have accurate drift detection with CloudFormation, include configurations \(enabled or disabled\) for all the 14 audit checks in your template\. For more information on the audit checks see [AWS::IoT::AccountAuditConfiguration AuditCheckConfigurations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iot-accountauditconfiguration-auditcheckconfigurations.html)\.

For more information, see [Detecting unmanaged configuration changes to stacks and resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift.html) in the *user guide*\.