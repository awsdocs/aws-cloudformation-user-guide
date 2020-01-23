# AWS::WAFv2::RuleGroup StatementTwos<a name="aws-properties-wafv2-rulegroup-statementtwos"></a>

Statements used in statement nesting\.

## Syntax<a name="aws-properties-wafv2-rulegroup-statementtwos-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-statementtwos-syntax.json"></a>

```
{
  "[StatementTwos](#cfn-wafv2-rulegroup-statementtwos-statementtwos)" : [ [StatementTwo](aws-properties-wafv2-rulegroup-statementtwo.md), ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-statementtwos-syntax.yaml"></a>

```
  [StatementTwos](#cfn-wafv2-rulegroup-statementtwos-statementtwos): 
    - [StatementTwo](aws-properties-wafv2-rulegroup-statementtwo.md)
```

## Properties<a name="aws-properties-wafv2-rulegroup-statementtwos-properties"></a>

`StatementTwos`  <a name="cfn-wafv2-rulegroup-statementtwos-statementtwos"></a>
Statements used in statement nesting\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-rulegroup-statementtwos) of [StatementTwo](aws-properties-wafv2-rulegroup-statementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)