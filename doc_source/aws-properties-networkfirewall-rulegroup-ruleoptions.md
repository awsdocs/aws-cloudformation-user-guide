# AWS::NetworkFirewall::RuleGroup RuleOptions<a name="aws-properties-networkfirewall-rulegroup-ruleoptions"></a>

Additional settings for a stateful rule, provided as keywords and settings\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-ruleoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-ruleoptions-syntax.json"></a>

```
{
  "[RuleOptions](#cfn-networkfirewall-rulegroup-ruleoptions-ruleoptions)" : [ RuleOption, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-ruleoptions-syntax.yaml"></a>

```
  [RuleOptions](#cfn-networkfirewall-rulegroup-ruleoptions-ruleoptions): 
    - RuleOption
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-ruleoptions-properties"></a>

`RuleOptions`  <a name="cfn-networkfirewall-rulegroup-ruleoptions-ruleoptions"></a>
Additional settings for a stateful rule, provided as keywords and settings\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-ruleoptions) of [RuleOption](aws-properties-networkfirewall-rulegroup-ruleoption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)