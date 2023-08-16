# AWS::FIS::ExperimentTemplate CloudWatchLogsConfiguration<a name="aws-properties-fis-experimenttemplate-cloudwatchlogsconfiguration"></a>

Specifies the configuration for experiment logging to CloudWatch Logs\.

## Syntax<a name="aws-properties-fis-experimenttemplate-cloudwatchlogsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fis-experimenttemplate-cloudwatchlogsconfiguration-syntax.json"></a>

```
{
  "[LogGroupArn](#cfn-fis-experimenttemplate-cloudwatchlogsconfiguration-loggrouparn)" : String
}
```

### YAML<a name="aws-properties-fis-experimenttemplate-cloudwatchlogsconfiguration-syntax.yaml"></a>

```
  [LogGroupArn](#cfn-fis-experimenttemplate-cloudwatchlogsconfiguration-loggrouparn): String
```

## Properties<a name="aws-properties-fis-experimenttemplate-cloudwatchlogsconfiguration-properties"></a>

`LogGroupArn`  <a name="cfn-fis-experimenttemplate-cloudwatchlogsconfiguration-loggrouparn"></a>
The Amazon Resource Name \(ARN\) of the destination Amazon CloudWatch Logs log group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `[\S]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)