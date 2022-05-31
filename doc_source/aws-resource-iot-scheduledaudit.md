# AWS::IoT::ScheduledAudit<a name="aws-resource-iot-scheduledaudit"></a>

Use the `AWS::IoT::ScheduledAudit` resource to create a scheduled audit that is run at a specified time interval\. For API reference, see [CreateScheduleAudit](https://docs.aws.amazon.com/iot/latest/apireference/API_CreateScheduledAudit.html) and for general information, see [Audit](https://docs.aws.amazon.com/iot/latest/developerguide/device-defender-audit.html)\.

## Syntax<a name="aws-resource-iot-scheduledaudit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-scheduledaudit-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::ScheduledAudit",
  "Properties" : {
      "[DayOfMonth](#cfn-iot-scheduledaudit-dayofmonth)" : String,
      "[DayOfWeek](#cfn-iot-scheduledaudit-dayofweek)" : String,
      "[Frequency](#cfn-iot-scheduledaudit-frequency)" : String,
      "[ScheduledAuditName](#cfn-iot-scheduledaudit-scheduledauditname)" : String,
      "[Tags](#cfn-iot-scheduledaudit-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetCheckNames](#cfn-iot-scheduledaudit-targetchecknames)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-iot-scheduledaudit-syntax.yaml"></a>

```
Type: AWS::IoT::ScheduledAudit
Properties: 
  [DayOfMonth](#cfn-iot-scheduledaudit-dayofmonth): String
  [DayOfWeek](#cfn-iot-scheduledaudit-dayofweek): String
  [Frequency](#cfn-iot-scheduledaudit-frequency): String
  [ScheduledAuditName](#cfn-iot-scheduledaudit-scheduledauditname): String
  [Tags](#cfn-iot-scheduledaudit-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetCheckNames](#cfn-iot-scheduledaudit-targetchecknames): 
    - String
```

## Properties<a name="aws-resource-iot-scheduledaudit-properties"></a>

`DayOfMonth`  <a name="cfn-iot-scheduledaudit-dayofmonth"></a>
The day of the month on which the scheduled audit is run \(if the `frequency` is "MONTHLY"\)\. If days 29\-31 are specified, and the month does not have that many days, the audit takes place on the "LAST" day of the month\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DayOfWeek`  <a name="cfn-iot-scheduledaudit-dayofweek"></a>
The day of the week on which the scheduled audit is run \(if the `frequency` is "WEEKLY" or "BIWEEKLY"\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Frequency`  <a name="cfn-iot-scheduledaudit-frequency"></a>
How often the scheduled audit occurs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduledAuditName`  <a name="cfn-iot-scheduledaudit-scheduledauditname"></a>
The name of the scheduled audit\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iot-scheduledaudit-tags"></a>
Metadata that can be used to manage the scheduled audit\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetCheckNames`  <a name="cfn-iot-scheduledaudit-targetchecknames"></a>
Which checks are performed during the scheduled audit\. Checks must be enabled for your account\. \(Use `DescribeAccountAuditConfiguration` to see the list of all checks, including those that are enabled or use `UpdateAccountAuditConfiguration` to select which checks are enabled\.\)  
 The following checks are currently aviable:   
+ `AUTHENTICATED_COGNITO_ROLE_OVERLY_PERMISSIVE_CHECK`
+ `CA_CERTIFICATE_EXPIRING_CHECK`
+ `CA_CERTIFICATE_KEY_QUALITY_CHECK`
+ `CONFLICTING_CLIENT_IDS_CHECK`
+ `DEVICE_CERTIFICATE_EXPIRING_CHECK`
+ `DEVICE_CERTIFICATE_KEY_QUALITY_CHECK`
+ `DEVICE_CERTIFICATE_SHARED_CHECK`
+ `IOT_POLICY_OVERLY_PERMISSIVE_CHECK`
+ `IOT_ROLE_ALIAS_ALLOWS_ACCESS_TO_UNUSED_SERVICES_CHECK`
+ `IOT_ROLE_ALIAS_OVERLY_PERMISSIVE_CHECK`
+ `LOGGING_DISABLED_CHECK`
+ `REVOKED_CA_CERTIFICATE_STILL_ACTIVE_CHECK`
+ `REVOKED_DEVICE_CERTIFICATE_STILL_ACTIVE_CHECK`
+ `UNAUTHENTICATED_COGNITO_ROLE_OVERLY_PERMISSIVE_CHECK`
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-scheduledaudit-return-values"></a>

### Ref<a name="aws-resource-iot-scheduledaudit-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the scheduled audit name\.

### Fn::GetAtt<a name="aws-resource-iot-scheduledaudit-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-scheduledaudit-return-values-fn--getatt-fn--getatt"></a>

`ScheduledAuditArn`  <a name="ScheduledAuditArn-fn::getatt"></a>
The ARN of the scheduled audit\.

## Examples<a name="aws-resource-iot-scheduledaudit--examples"></a>

In this ScheduledAudit example, all audit checks are enabled, the frequency of the audit is weekly, and the audit will occur every Monday\.

### <a name="aws-resource-iot-scheduledaudit--examples--"></a>



#### JSON<a name="aws-resource-iot-scheduledaudit--examples----json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "Amazon Web Services IoT ScheduledAudit Sample Template",
  "Resources": {
    "MyScheduledAudit": {
      "Type": "AWS::IoT::ScheduledAudit",
      "Properties": {
        "ScheduledAuditName": "MyScheduledAudit",
        "DayOfWeek" : "MON",
        "Frequency" : "WEEKLY",
        "TargetCheckNames": [
           "AUTHENTICATED_COGNITO_ROLE_OVERLY_PERMISSIVE_CHECK",
           "CA_CERTIFICATE_EXPIRING_CHECK",
           "CA_CERTIFICATE_KEY_QUALITY_CHECK",
           "CONFLICTING_CLIENT_IDS_CHECK",
           "DEVICE_CERTIFICATE_EXPIRING_CHECK",
           "DEVICE_CERTIFICATE_KEY_QUALITY_CHECK",
           "DEVICE_CERTIFICATE_SHARED_CHECK",
           "IOT_POLICY_OVERLY_PERMISSIVE_CHECK",
           "IOT_ROLE_ALIAS_ALLOWS_ACCESS_TO_UNUSED_SERVICES_CHECK",
           "IOT_ROLE_ALIAS_OVERLY_PERMISSIVE_CHECK",
           "LOGGING_DISABLED_CHECK",
           "REVOKED_CA_CERTIFICATE_STILL_ACTIVE_CHECK",
           "REVOKED_DEVICE_CERTIFICATE_STILL_ACTIVE_CHECK",
           "UNAUTHENTICATED_COGNITO_ROLE_OVERLY_PERMISSIVE_CHECK" 
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-iot-scheduledaudit--examples----yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Amazon Web Services IoT ScheduledAudit Sample Template
Resources:
  MyScheduledAudit:
    Type: AWS::IoT::ScheduledAudit
    Properties:
      ScheduledAuditName: MyScheduledAudit
      DayOfWeek: 'MON'
      Frequency: WEEKLY
      TargetCheckNames:
      - AUTHENTICATED_COGNITO_ROLE_OVERLY_PERMISSIVE_CHECK
      - CA_CERTIFICATE_EXPIRING_CHECK
      - CA_CERTIFICATE_KEY_QUALITY_CHECK
      - CONFLICTING_CLIENT_IDS_CHECK
      - DEVICE_CERTIFICATE_EXPIRING_CHECK
      - DEVICE_CERTIFICATE_KEY_QUALITY_CHECK
      - DEVICE_CERTIFICATE_SHARED_CHECK
      - IOT_POLICY_OVERLY_PERMISSIVE_CHECK
      - IOT_ROLE_ALIAS_ALLOWS_ACCESS_TO_UNUSED_SERVICES_CHECK
      - IOT_ROLE_ALIAS_OVERLY_PERMISSIVE_CHECK
      - LOGGING_DISABLED_CHECK
      - REVOKED_CA_CERTIFICATE_STILL_ACTIVE_CHECK
      - REVOKED_DEVICE_CERTIFICATE_STILL_ACTIVE_CHECK
      - UNAUTHENTICATED_COGNITO_ROLE_OVERLY_PERMISSIVE_CHECK
```

## See also<a name="aws-resource-iot-scheduledaudit--seealso"></a>

For more information on audit checks see [AWS::IoT::AccountAuditConfiguration AuditCheckConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iot-accountauditconfiguration-auditcheckconfigurations.html)\.