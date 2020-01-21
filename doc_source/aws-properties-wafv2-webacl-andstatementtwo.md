# AWS::WAFv2::WebACL AndStatementTwo<a name="aws-properties-wafv2-webacl-andstatementtwo"></a>

Logical AND statement used in statement nesting\.

## Syntax<a name="aws-properties-wafv2-webacl-andstatementtwo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-andstatementtwo-syntax.json"></a>

```
{
  "[Statements](#cfn-wafv2-webacl-andstatementtwo-statements)" : [StatementThrees](aws-properties-wafv2-webacl-statementthrees.md)
}
```

### YAML<a name="aws-properties-wafv2-webacl-andstatementtwo-syntax.yaml"></a>

```
  [Statements](#cfn-wafv2-webacl-andstatementtwo-statements): 
    [StatementThrees](aws-properties-wafv2-webacl-statementthrees.md)
```

## Properties<a name="aws-properties-wafv2-webacl-andstatementtwo-properties"></a>

`Statements`  <a name="cfn-wafv2-webacl-andstatementtwo-statements"></a>
Logical AND statements used in statement nesting\.  
*Required*: No  
*Type*: [StatementThrees](aws-properties-wafv2-webacl-statementthrees.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)