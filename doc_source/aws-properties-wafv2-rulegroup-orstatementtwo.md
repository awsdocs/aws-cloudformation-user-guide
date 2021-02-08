# AWS::WAFv2::RuleGroup OrStatementTwo<a name="aws-properties-wafv2-rulegroup-orstatementtwo"></a>

Logical OR statement used in statement nesting\.

## Syntax<a name="aws-properties-wafv2-rulegroup-orstatementtwo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-orstatementtwo-syntax.json"></a>

```
{
  "[Statements](#cfn-wafv2-rulegroup-orstatementtwo-statements)" : [ StatementThree, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-orstatementtwo-syntax.yaml"></a>

```
  [Statements](#cfn-wafv2-rulegroup-orstatementtwo-statements): 
    - StatementThree
```

## Properties<a name="aws-properties-wafv2-rulegroup-orstatementtwo-properties"></a>

`Statements`  <a name="cfn-wafv2-rulegroup-orstatementtwo-statements"></a>
Logical OR statements used in statement nesting\.  
*Required*: Yes  
*Type*: List of [StatementThree](aws-properties-wafv2-rulegroup-statementthree.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)