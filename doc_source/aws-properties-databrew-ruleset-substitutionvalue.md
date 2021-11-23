# AWS::DataBrew::Ruleset SubstitutionValue<a name="aws-properties-databrew-ruleset-substitutionvalue"></a>

A key\-value pair to associate an expression's substitution variable names with their values\.

## Syntax<a name="aws-properties-databrew-ruleset-substitutionvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-ruleset-substitutionvalue-syntax.json"></a>

```
{
  "[Value](#cfn-databrew-ruleset-substitutionvalue-value)" : String,
  "[ValueReference](#cfn-databrew-ruleset-substitutionvalue-valuereference)" : String
}
```

### YAML<a name="aws-properties-databrew-ruleset-substitutionvalue-syntax.yaml"></a>

```
  [Value](#cfn-databrew-ruleset-substitutionvalue-value): String
  [ValueReference](#cfn-databrew-ruleset-substitutionvalue-valuereference): String
```

## Properties<a name="aws-properties-databrew-ruleset-substitutionvalue-properties"></a>

`Value`  <a name="cfn-databrew-ruleset-substitutionvalue-value"></a>
Value or column name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueReference`  <a name="cfn-databrew-ruleset-substitutionvalue-valuereference"></a>
Variable name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)