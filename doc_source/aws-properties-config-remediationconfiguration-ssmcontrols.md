# AWS::Config::RemediationConfiguration SsmControls<a name="aws-properties-config-remediationconfiguration-ssmcontrols"></a>

<a name="aws-properties-config-remediationconfiguration-ssmcontrols-description"></a>The `SsmControls` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::Config::RemediationConfiguration](aws-resource-config-remediationconfiguration.md)\.

## Syntax<a name="aws-properties-config-remediationconfiguration-ssmcontrols-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-remediationconfiguration-ssmcontrols-syntax.json"></a>

```
{
  "[ConcurrentExecutionRatePercentage](#cfn-config-remediationconfiguration-ssmcontrols-concurrentexecutionratepercentage)" : Integer,
  "[ErrorPercentage](#cfn-config-remediationconfiguration-ssmcontrols-errorpercentage)" : Integer
}
```

### YAML<a name="aws-properties-config-remediationconfiguration-ssmcontrols-syntax.yaml"></a>

```
  [ConcurrentExecutionRatePercentage](#cfn-config-remediationconfiguration-ssmcontrols-concurrentexecutionratepercentage): Integer
  [ErrorPercentage](#cfn-config-remediationconfiguration-ssmcontrols-errorpercentage): Integer
```

## Properties<a name="aws-properties-config-remediationconfiguration-ssmcontrols-properties"></a>

`ConcurrentExecutionRatePercentage`  <a name="cfn-config-remediationconfiguration-ssmcontrols-concurrentexecutionratepercentage"></a>
The maximum percentage of remediation actions allowed to run in parallel on the non\-compliant resources for that specific rule\. You can specify a percentage, such as 10%\. The default value is 10\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorPercentage`  <a name="cfn-config-remediationconfiguration-ssmcontrols-errorpercentage"></a>
The percentage of errors that are allowed before SSM stops running automations on non\-compliant resources for that specific rule\. You can specify a percentage of errors, for example 10%\. If you do not specifiy a percentage, the default is 50%\. For example, if you set the ErrorPercentage to 40% for 10 non\-compliant resources, then SSM stops running the automations when the fifth error is received\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)