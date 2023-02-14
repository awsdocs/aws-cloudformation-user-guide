# AWS::CloudFormation::HookVersion LoggingConfig<a name="aws-properties-cloudformation-hookversion-loggingconfig"></a>

The `LoggingConfig` property type specifies logging configuration information for an extension\.

## Syntax<a name="aws-properties-cloudformation-hookversion-loggingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudformation-hookversion-loggingconfig-syntax.json"></a>

```
{
  "[LogGroupName](#cfn-cloudformation-hookversion-loggingconfig-loggroupname)" : String,
  "[LogRoleArn](#cfn-cloudformation-hookversion-loggingconfig-logrolearn)" : String
}
```

### YAML<a name="aws-properties-cloudformation-hookversion-loggingconfig-syntax.yaml"></a>

```
  [LogGroupName](#cfn-cloudformation-hookversion-loggingconfig-loggroupname): String
  [LogRoleArn](#cfn-cloudformation-hookversion-loggingconfig-logrolearn): String
```

## Properties<a name="aws-properties-cloudformation-hookversion-loggingconfig-properties"></a>

`LogGroupName`  <a name="cfn-cloudformation-hookversion-loggingconfig-loggroupname"></a>
The Amazon CloudWatch Logs group to which CloudFormation sends error logging information when invoking the extension's handlers\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\.\-_/#A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogRoleArn`  <a name="cfn-cloudformation-hookversion-loggingconfig-logrolearn"></a>
The Amazon Resource Name \(ARN\) of the role that CloudFormation should assume when sending log entries to CloudWatch Logs\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `arn:.+:iam::[0-9]{12}:role/.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)