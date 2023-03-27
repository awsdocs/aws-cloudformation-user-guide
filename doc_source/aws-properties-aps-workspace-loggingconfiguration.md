# AWS::APS::Workspace LoggingConfiguration<a name="aws-properties-aps-workspace-loggingconfiguration"></a>

The LoggingConfiguration attribute sets the logging configuration for the workspace\.

## Syntax<a name="aws-properties-aps-workspace-loggingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-aps-workspace-loggingconfiguration-syntax.json"></a>

```
{
  "[LogGroupArn](#cfn-aps-workspace-loggingconfiguration-loggrouparn)" : String
}
```

### YAML<a name="aws-properties-aps-workspace-loggingconfiguration-syntax.yaml"></a>

```
  [LogGroupArn](#cfn-aps-workspace-loggingconfiguration-loggrouparn): String
```

## Properties<a name="aws-properties-aps-workspace-loggingconfiguration-properties"></a>

`LogGroupArn`  <a name="cfn-aps-workspace-loggingconfiguration-loggrouparn"></a>
The Amazon Resource Name \(ARN\) of the CloudWatch log group the logs are emitted to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)