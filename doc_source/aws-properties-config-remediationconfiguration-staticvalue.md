# AWS::Config::RemediationConfiguration StaticValue<a name="aws-properties-config-remediationconfiguration-staticvalue"></a>

The static value of the resource\.

## Syntax<a name="aws-properties-config-remediationconfiguration-staticvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-remediationconfiguration-staticvalue-syntax.json"></a>

```
{
  "[Values](#cfn-config-remediationconfiguration-staticvalue-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-config-remediationconfiguration-staticvalue-syntax.yaml"></a>

```
  [Values](#cfn-config-remediationconfiguration-staticvalue-values): 
    - String
```

## Properties<a name="aws-properties-config-remediationconfiguration-staticvalue-properties"></a>

`Values`  <a name="cfn-config-remediationconfiguration-staticvalue-values"></a>
A list of values\. For example, the ARN of the assumed role\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)