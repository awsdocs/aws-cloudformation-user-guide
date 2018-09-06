# AWS CodeDeploy DeploymentGroup AlarmConfiguration<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration"></a>

The `AlarmConfiguration` property type configures CloudWatch alarms for an AWS CodeDeploy deployment group\. `AlarmConfiguration` is a property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration-syntax.json"></a>

```
{
  "[Alarms](#cfn-codedeploy-deploymentgroup-alarmconfiguration-alarms)" : [ [*Alarm*](aws-properties-codedeploy-deploymentgroup-alarm.md), ... ],
  "[Enabled](#cfn-codedeploy-deploymentgroup-alarmconfiguration-enabled)" : Boolean,
  "[IgnorePollAlarmFailure](#cfn-codedeploy-deploymentgroup-alarmconfiguration-ignorepollalarmfailure)" : Boolean
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration-syntax.yaml"></a>

```
[Alarms](#cfn-codedeploy-deploymentgroup-alarmconfiguration-alarms):
  - [*Alarm*](aws-properties-codedeploy-deploymentgroup-alarm.md)
[Enabled](#cfn-codedeploy-deploymentgroup-alarmconfiguration-enabled): Boolean
[IgnorePollAlarmFailure](#cfn-codedeploy-deploymentgroup-alarmconfiguration-ignorepollalarmfailure): Boolean
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-alarmconfiguration-properties"></a>

For more information about each property, including constraints and valid values, see [AlarmConfiguration](http://docs.aws.amazon.com//codedeploy/latest/APIReference/API_AlarmConfiguration.html) in the *AWS CodeDeploy API Reference*\.

`Alarms`  <a name="cfn-codedeploy-deploymentgroup-alarmconfiguration-alarms"></a>
The list of alarms configured for the deployment group\. Duplicates are not allowed\.  
*Required*: No  
*Type*: List of [AWS CodeDeploy DeploymentGroup Alarm](aws-properties-codedeploy-deploymentgroup-alarm.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Enabled`  <a name="cfn-codedeploy-deploymentgroup-alarmconfiguration-enabled"></a>
Indicates whether the alarm configuration is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IgnorePollAlarmFailure`  <a name="cfn-codedeploy-deploymentgroup-alarmconfiguration-ignorepollalarmfailure"></a>
Indicates whether a deployment should continue if information about the current state of alarms cannot be retrieved from CloudWatch\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)