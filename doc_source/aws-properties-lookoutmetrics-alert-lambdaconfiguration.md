# AWS::LookoutMetrics::Alert LambdaConfiguration<a name="aws-properties-lookoutmetrics-alert-lambdaconfiguration"></a>

Contains information about a Lambda configuration\.

## Syntax<a name="aws-properties-lookoutmetrics-alert-lambdaconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-alert-lambdaconfiguration-syntax.json"></a>

```
{
  "[LambdaArn](#cfn-lookoutmetrics-alert-lambdaconfiguration-lambdaarn)" : String,
  "[RoleArn](#cfn-lookoutmetrics-alert-lambdaconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-lookoutmetrics-alert-lambdaconfiguration-syntax.yaml"></a>

```
  [LambdaArn](#cfn-lookoutmetrics-alert-lambdaconfiguration-lambdaarn): String
  [RoleArn](#cfn-lookoutmetrics-alert-lambdaconfiguration-rolearn): String
```

## Properties<a name="aws-properties-lookoutmetrics-alert-lambdaconfiguration-properties"></a>

`LambdaArn`  <a name="cfn-lookoutmetrics-alert-lambdaconfiguration-lambdaarn"></a>
The ARN of the Lambda function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-lookoutmetrics-alert-lambdaconfiguration-rolearn"></a>
The ARN of an IAM role that has permission to invoke the Lambda function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)