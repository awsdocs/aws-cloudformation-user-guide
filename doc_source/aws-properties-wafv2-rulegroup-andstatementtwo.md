# AWS::WAFv2::RuleGroup AndStatementTwo<a name="aws-properties-wafv2-rulegroup-andstatementtwo"></a>

Logical AND statement used in statement nesting\.

## Syntax<a name="aws-properties-wafv2-rulegroup-andstatementtwo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-andstatementtwo-syntax.json"></a>

```
{
  "[Statements](#cfn-wafv2-rulegroup-andstatementtwo-statements)" : [StatementThrees](aws-properties-wafv2-rulegroup-statementthrees.md)
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-andstatementtwo-syntax.yaml"></a>

```
  [Statements](#cfn-wafv2-rulegroup-andstatementtwo-statements): 
    [StatementThrees](aws-properties-wafv2-rulegroup-statementthrees.md)
```

## Properties<a name="aws-properties-wafv2-rulegroup-andstatementtwo-properties"></a>

`Statements`  <a name="cfn-wafv2-rulegroup-andstatementtwo-statements"></a>
Logical AND statements used in statement nesting\.  
*Required*: No  
*Type*: [StatementThrees](aws-properties-wafv2-rulegroup-statementthrees.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)