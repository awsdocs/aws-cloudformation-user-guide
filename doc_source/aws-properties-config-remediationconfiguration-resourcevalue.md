# AWS::Config::RemediationConfiguration ResourceValue<a name="aws-properties-config-remediationconfiguration-resourcevalue"></a>

The dynamic value of the resource\.

## Syntax<a name="aws-properties-config-remediationconfiguration-resourcevalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-remediationconfiguration-resourcevalue-syntax.json"></a>

```
{
  "[Value](#cfn-config-remediationconfiguration-resourcevalue-value)" : String
}
```

### YAML<a name="aws-properties-config-remediationconfiguration-resourcevalue-syntax.yaml"></a>

```
  [Value](#cfn-config-remediationconfiguration-resourcevalue-value): String
```

## Properties<a name="aws-properties-config-remediationconfiguration-resourcevalue-properties"></a>

`Value`  <a name="cfn-config-remediationconfiguration-resourcevalue-value"></a>
The value is a resource ID\.  
*Required*: No  
*Type*: String  
*Allowed values*: `RESOURCE_ID`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)