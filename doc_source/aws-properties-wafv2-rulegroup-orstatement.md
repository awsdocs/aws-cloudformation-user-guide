# AWS::WAFv2::RuleGroup OrStatement<a name="aws-properties-wafv2-rulegroup-orstatement"></a>

A logical rule statement used to combine other rule statements with OR logic\. You provide more than one `Statement` within the `OrStatement`\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-orstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-orstatement-syntax.json"></a>

```
{
  "[Statements](#cfn-wafv2-rulegroup-orstatement-statements)" : [ Statement, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-orstatement-syntax.yaml"></a>

```
  [Statements](#cfn-wafv2-rulegroup-orstatement-statements): 
    - Statement
```

## Properties<a name="aws-properties-wafv2-rulegroup-orstatement-properties"></a>

`Statements`  <a name="cfn-wafv2-rulegroup-orstatement-statements"></a>
The statements to combine with OR logic\. You can use any statements that can be nested\.  
*Required*: Yes  
*Type*: List of [Statement](aws-properties-wafv2-rulegroup-statement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)