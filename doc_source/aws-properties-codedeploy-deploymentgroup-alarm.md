# AWS CodeDeploy DeploymentGroup Alarm<a name="aws-properties-codedeploy-deploymentgroup-alarm"></a>

The `Alarm` property type specifies a CloudWatch alarm to use for an AWS CodeDeploy deployment group\. The `Alarm` property of the [AWS CodeDeploy DeploymentGroup AlarmConfiguration](aws-properties-codedeploy-deploymentgroup-alarmconfiguration.md) property contains a list of `Alarm` property types\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-alarm-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-alarm-syntax.json"></a>

```
{
  "[Name](#cfn-codedeploy-deploymentgroup-alarm-name)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-alarm-syntax.yaml"></a>

```
[Name](#cfn-codedeploy-deploymentgroup-alarm-name): String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-alarm-properties"></a>

`Name`  <a name="cfn-codedeploy-deploymentgroup-alarm-name"></a>
The name of the alarm\. For more information, see [Alarm](http://docs.aws.amazon.com//codedeploy/latest/APIReference/API_Alarm.html) in the *AWS CodeDeploy API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)