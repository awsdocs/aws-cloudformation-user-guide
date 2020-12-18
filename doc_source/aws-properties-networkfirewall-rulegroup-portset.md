# AWS::NetworkFirewall::RuleGroup PortSet<a name="aws-properties-networkfirewall-rulegroup-portset"></a>

A set of port ranges for use in the rules in a rule group\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-portset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-portset-syntax.json"></a>

```
{
  "[Definition](#cfn-networkfirewall-rulegroup-portset-definition)" : VariableDefinitionList
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-portset-syntax.yaml"></a>

```
  [Definition](#cfn-networkfirewall-rulegroup-portset-definition): 
    VariableDefinitionList
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-portset-properties"></a>

`Definition`  <a name="cfn-networkfirewall-rulegroup-portset-definition"></a>
The set of port ranges\.   
*Required*: No  
*Type*: [VariableDefinitionList](aws-properties-networkfirewall-rulegroup-variabledefinitionlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)