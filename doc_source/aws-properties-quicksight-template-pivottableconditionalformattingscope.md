# AWS::QuickSight::Template PivotTableConditionalFormattingScope<a name="aws-properties-quicksight-template-pivottableconditionalformattingscope"></a>

The scope of the cell for conditional formatting\.

## Syntax<a name="aws-properties-quicksight-template-pivottableconditionalformattingscope-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-pivottableconditionalformattingscope-syntax.json"></a>

```
{
  "[Role](#cfn-quicksight-template-pivottableconditionalformattingscope-role)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-pivottableconditionalformattingscope-syntax.yaml"></a>

```
  [Role](#cfn-quicksight-template-pivottableconditionalformattingscope-role): String
```

## Properties<a name="aws-properties-quicksight-template-pivottableconditionalformattingscope-properties"></a>

`Role`  <a name="cfn-quicksight-template-pivottableconditionalformattingscope-role"></a>
The role \(field, field total, grand total\) of the cell for conditional formatting\.  
*Required*: No  
*Type*: String  
*Allowed values*: `FIELD | FIELD_TOTAL | GRAND_TOTAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)