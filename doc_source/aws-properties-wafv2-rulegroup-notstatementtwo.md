# AWS::WAFv2::RuleGroup NotStatementTwo<a name="aws-properties-wafv2-rulegroup-notstatementtwo"></a>

Logical NOT statement used to negate the match results of a nested statement\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-notstatementtwo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-notstatementtwo-syntax.json"></a>

```
{
  "[Statement](#cfn-wafv2-rulegroup-notstatementtwo-statement)" : StatementThree
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-notstatementtwo-syntax.yaml"></a>

```
  [Statement](#cfn-wafv2-rulegroup-notstatementtwo-statement): 
    StatementThree
```

## Properties<a name="aws-properties-wafv2-rulegroup-notstatementtwo-properties"></a>

`Statement`  <a name="cfn-wafv2-rulegroup-notstatementtwo-statement"></a>
Logical NOT statement used to negate the match results of a nested statement\.   
*Required*: Yes  
*Type*: [StatementThree](aws-properties-wafv2-rulegroup-statementthree.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)