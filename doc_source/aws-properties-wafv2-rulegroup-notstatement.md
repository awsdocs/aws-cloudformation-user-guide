# AWS::WAFv2::RuleGroup NotStatement<a name="aws-properties-wafv2-rulegroup-notstatement"></a>

A logical rule statement used to negate the results of another rule statement\. You provide one `Statement` within the `NotStatement`\.

## Syntax<a name="aws-properties-wafv2-rulegroup-notstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-notstatement-syntax.json"></a>

```
{
  "[Statement](#cfn-wafv2-rulegroup-notstatement-statement)" : Statement
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-notstatement-syntax.yaml"></a>

```
  [Statement](#cfn-wafv2-rulegroup-notstatement-statement): 
    Statement
```

## Properties<a name="aws-properties-wafv2-rulegroup-notstatement-properties"></a>

`Statement`  <a name="cfn-wafv2-rulegroup-notstatement-statement"></a>
The statement to negate\. You can use any statement that can be nested\.  
*Required*: Yes  
*Type*: [Statement](aws-properties-wafv2-rulegroup-statement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)