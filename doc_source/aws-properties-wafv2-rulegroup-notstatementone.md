# AWS::WAFv2::RuleGroup NotStatementOne<a name="aws-properties-wafv2-rulegroup-notstatementone"></a>

Logical NOT statement used to negate the match results of a nested statement\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-notstatementone-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-notstatementone-syntax.json"></a>

```
{
  "[Statement](#cfn-wafv2-rulegroup-notstatementone-statement)" : StatementTwo
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-notstatementone-syntax.yaml"></a>

```
  [Statement](#cfn-wafv2-rulegroup-notstatementone-statement): 
    StatementTwo
```

## Properties<a name="aws-properties-wafv2-rulegroup-notstatementone-properties"></a>

`Statement`  <a name="cfn-wafv2-rulegroup-notstatementone-statement"></a>
Logical NOT statement used to negate the match results of a nested statement\.   
*Required*: Yes  
*Type*: [StatementTwo](aws-properties-wafv2-rulegroup-statementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)