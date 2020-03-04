# AWS::WAFv2::WebACL StatementThrees<a name="aws-properties-wafv2-webacl-statementthrees"></a>

Statements used in statement nesting\.

## Syntax<a name="aws-properties-wafv2-webacl-statementthrees-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-statementthrees-syntax.json"></a>

```
{
  "[StatementThrees](#cfn-wafv2-webacl-statementthrees-statementthrees)" : [ [StatementThree](aws-properties-wafv2-webacl-statementthree.md), ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-statementthrees-syntax.yaml"></a>

```
  [StatementThrees](#cfn-wafv2-webacl-statementthrees-statementthrees): 
    - [StatementThree](aws-properties-wafv2-webacl-statementthree.md)
```

## Properties<a name="aws-properties-wafv2-webacl-statementthrees-properties"></a>

`StatementThrees`  <a name="cfn-wafv2-webacl-statementthrees-statementthrees"></a>
Statements used in statement nesting\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-webacl-statementthrees) of [StatementThree](aws-properties-wafv2-webacl-statementthree.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)