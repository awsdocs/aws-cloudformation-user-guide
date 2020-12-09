# AWS::CodeDeploy::DeploymentGroup Alarm<a name="aws-properties-codedeploy-deploymentgroup-alarm"></a>

 The `Alarm` property type specifies a CloudWatch alarm to use for an AWS CodeDeploy deployment group\. The `Alarm` property of the [ CodeDeploy DeploymentGroup AlarmConfiguration ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codedeploy-deploymentgroup-alarmconfiguration.html) property contains a list of `Alarm` property types\. 

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
The name of the alarm\. Maximum length is 255 characters\. Each alarm name can be used only once in a list of alarms\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)