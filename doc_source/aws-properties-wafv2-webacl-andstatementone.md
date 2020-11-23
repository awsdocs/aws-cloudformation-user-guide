# AWS::WAFv2::WebACL AndStatementOne<a name="aws-properties-wafv2-webacl-andstatementone"></a>

Logical AND statement used in statement nesting\.

## Syntax<a name="aws-properties-wafv2-webacl-andstatementone-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-andstatementone-syntax.json"></a>

```
{
  "[Statements](#cfn-wafv2-webacl-andstatementone-statements)" : [ StatementTwo, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-andstatementone-syntax.yaml"></a>

```
  [Statements](#cfn-wafv2-webacl-andstatementone-statements): 
    - StatementTwo
```

## Properties<a name="aws-properties-wafv2-webacl-andstatementone-properties"></a>

`Statements`  <a name="cfn-wafv2-webacl-andstatementone-statements"></a>
Logical AND statements used in statement nesting\.  
*Required*: Yes  
*Type*: List of [StatementTwo](aws-properties-wafv2-webacl-statementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)