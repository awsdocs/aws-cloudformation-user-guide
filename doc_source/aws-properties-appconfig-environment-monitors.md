# AWS::AppConfig::Environment Monitors<a name="aws-properties-appconfig-environment-monitors"></a>

Amazon CloudWatch alarms to monitor during the deployment process\.

## Syntax<a name="aws-properties-appconfig-environment-monitors-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appconfig-environment-monitors-syntax.json"></a>

```
{
  "[AlarmArn](#cfn-appconfig-environment-monitors-alarmarn)" : String,
  "[AlarmRoleArn](#cfn-appconfig-environment-monitors-alarmrolearn)" : String
}
```

### YAML<a name="aws-properties-appconfig-environment-monitors-syntax.yaml"></a>

```
  [AlarmArn](#cfn-appconfig-environment-monitors-alarmarn): String
  [AlarmRoleArn](#cfn-appconfig-environment-monitors-alarmrolearn): String
```

## Properties<a name="aws-properties-appconfig-environment-monitors-properties"></a>

`AlarmArn`  <a name="cfn-appconfig-environment-monitors-alarmarn"></a>
ARN of the Amazon CloudWatch alarm\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:(aws[a-zA-Z-]*)?:[a-z]+:([a-z]{2}((-gov)|(-iso(b?)))?-[a-z]+-\d{1})?:(\d{12})?:[a-zA-Z0-9-_/:.]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmRoleArn`  <a name="cfn-appconfig-environment-monitors-alarmrolearn"></a>
ARN of an IAM role for AWS AppConfig to monitor `AlarmArn`\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^((arn):(aws|aws-cn|aws-iso|aws-iso-[a-z]{1}|aws-us-gov):(iam)::\d{12}:role[/].*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)