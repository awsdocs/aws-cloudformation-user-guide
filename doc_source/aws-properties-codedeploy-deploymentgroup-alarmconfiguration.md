# AWS::CodeDeploy::DeploymentGroup AlarmConfiguration<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration"></a>

 The `AlarmConfiguration` property type configuresCloudWatch alarms for an AWS CodeDeploy deployment group\. `AlarmConfiguration` is a property of the [DeploymentGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html) resource\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration-syntax.json"></a>

```
{
  "[Alarms](#cfn-codedeploy-deploymentgroup-alarmconfiguration-alarms)" : [ Alarm, ... ],
  "[Enabled](#cfn-codedeploy-deploymentgroup-alarmconfiguration-enabled)" : Boolean,
  "[IgnorePollAlarmFailure](#cfn-codedeploy-deploymentgroup-alarmconfiguration-ignorepollalarmfailure)" : Boolean
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration-syntax.yaml"></a>

```
  [Alarms](#cfn-codedeploy-deploymentgroup-alarmconfiguration-alarms): 
    - Alarm
  [Enabled](#cfn-codedeploy-deploymentgroup-alarmconfiguration-enabled): Boolean
  [IgnorePollAlarmFailure](#cfn-codedeploy-deploymentgroup-alarmconfiguration-ignorepollalarmfailure): Boolean
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration-properties"></a>

`Alarms`  <a name="cfn-codedeploy-deploymentgroup-alarmconfiguration-alarms"></a>
A list of alarms configured for the deployment group\. A maximum of 10 alarms can be added to a deployment group\.  
*Required*: No  
*Type*: List of [Alarm](aws-properties-codedeploy-deploymentgroup-alarm.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-codedeploy-deploymentgroup-alarmconfiguration-enabled"></a>
Indicates whether the alarm configuration is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IgnorePollAlarmFailure`  <a name="cfn-codedeploy-deploymentgroup-alarmconfiguration-ignorepollalarmfailure"></a>
Indicates whether a deployment should continue if information about the current state of alarms cannot be retrieved from Amazon CloudWatch\. The default value is `false`\.  
+  `true`: The deployment proceeds even if alarm status information can't be retrieved from Amazon CloudWatch\.
+  `false`: The deployment stops if alarm status information can't be retrieved from Amazon CloudWatch\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)