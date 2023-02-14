# AWS::LookoutMetrics::Alert Action<a name="aws-properties-lookoutmetrics-alert-action"></a>

A configuration that specifies the action to perform when anomalies are detected\.

## Syntax<a name="aws-properties-lookoutmetrics-alert-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-alert-action-syntax.json"></a>

```
{
  "[LambdaConfiguration](#cfn-lookoutmetrics-alert-action-lambdaconfiguration)" : LambdaConfiguration,
  "[SNSConfiguration](#cfn-lookoutmetrics-alert-action-snsconfiguration)" : SNSConfiguration
}
```

### YAML<a name="aws-properties-lookoutmetrics-alert-action-syntax.yaml"></a>

```
  [LambdaConfiguration](#cfn-lookoutmetrics-alert-action-lambdaconfiguration): 
    LambdaConfiguration
  [SNSConfiguration](#cfn-lookoutmetrics-alert-action-snsconfiguration): 
    SNSConfiguration
```

## Properties<a name="aws-properties-lookoutmetrics-alert-action-properties"></a>

`LambdaConfiguration`  <a name="cfn-lookoutmetrics-alert-action-lambdaconfiguration"></a>
A configuration for an AWS Lambda channel\.  
*Required*: No  
*Type*: [LambdaConfiguration](aws-properties-lookoutmetrics-alert-lambdaconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SNSConfiguration`  <a name="cfn-lookoutmetrics-alert-action-snsconfiguration"></a>
A configuration for an Amazon SNS channel\.  
*Required*: No  
*Type*: [SNSConfiguration](aws-properties-lookoutmetrics-alert-snsconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)