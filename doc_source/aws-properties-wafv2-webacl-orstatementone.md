# AWS::WAFv2::WebACL OrStatementOne<a name="aws-properties-wafv2-webacl-orstatementone"></a>

Logical OR statement\.

## Syntax<a name="aws-properties-wafv2-webacl-orstatementone-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-orstatementone-syntax.json"></a>

```
{
  "[Statements](#cfn-wafv2-webacl-orstatementone-statements)" : [ StatementTwo, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-orstatementone-syntax.yaml"></a>

```
  [Statements](#cfn-wafv2-webacl-orstatementone-statements): 
    - StatementTwo
```

## Properties<a name="aws-properties-wafv2-webacl-orstatementone-properties"></a>

`Statements`  <a name="cfn-wafv2-webacl-orstatementone-statements"></a>
Logical OR statement used in statement nesting\.  
*Required*: Yes  
*Type*: List of [StatementTwo](aws-properties-wafv2-webacl-statementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)