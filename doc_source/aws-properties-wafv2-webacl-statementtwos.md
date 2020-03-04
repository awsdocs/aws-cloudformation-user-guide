# AWS::WAFv2::WebACL StatementTwos<a name="aws-properties-wafv2-webacl-statementtwos"></a>

Statements used in statement nesting\.

## Syntax<a name="aws-properties-wafv2-webacl-statementtwos-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-statementtwos-syntax.json"></a>

```
{
  "[StatementTwos](#cfn-wafv2-webacl-statementtwos-statementtwos)" : [ [StatementTwo](aws-properties-wafv2-webacl-statementtwo.md), ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-statementtwos-syntax.yaml"></a>

```
  [StatementTwos](#cfn-wafv2-webacl-statementtwos-statementtwos): 
    - [StatementTwo](aws-properties-wafv2-webacl-statementtwo.md)
```

## Properties<a name="aws-properties-wafv2-webacl-statementtwos-properties"></a>

`StatementTwos`  <a name="cfn-wafv2-webacl-statementtwos-statementtwos"></a>
Statements used in statement nesting\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-webacl-statementtwos) of [StatementTwo](aws-properties-wafv2-webacl-statementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)