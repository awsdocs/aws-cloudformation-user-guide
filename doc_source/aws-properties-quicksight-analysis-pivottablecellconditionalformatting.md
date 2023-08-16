# AWS::QuickSight::Analysis PivotTableCellConditionalFormatting<a name="aws-properties-quicksight-analysis-pivottablecellconditionalformatting"></a>

The cell conditional formatting option for a pivot table\.

## Syntax<a name="aws-properties-quicksight-analysis-pivottablecellconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-pivottablecellconditionalformatting-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-analysis-pivottablecellconditionalformatting-fieldid)" : String,
  "[Scope](#cfn-quicksight-analysis-pivottablecellconditionalformatting-scope)" : PivotTableConditionalFormattingScope,
  "[Scopes](#cfn-quicksight-analysis-pivottablecellconditionalformatting-scopes)" : [ PivotTableConditionalFormattingScope, ... ],
  "[TextFormat](#cfn-quicksight-analysis-pivottablecellconditionalformatting-textformat)" : TextConditionalFormat
}
```

### YAML<a name="aws-properties-quicksight-analysis-pivottablecellconditionalformatting-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-analysis-pivottablecellconditionalformatting-fieldid): String
  [Scope](#cfn-quicksight-analysis-pivottablecellconditionalformatting-scope): 
    PivotTableConditionalFormattingScope
  [Scopes](#cfn-quicksight-analysis-pivottablecellconditionalformatting-scopes): 
    - PivotTableConditionalFormattingScope
  [TextFormat](#cfn-quicksight-analysis-pivottablecellconditionalformatting-textformat): 
    TextConditionalFormat
```

## Properties<a name="aws-properties-quicksight-analysis-pivottablecellconditionalformatting-properties"></a>

`FieldId`  <a name="cfn-quicksight-analysis-pivottablecellconditionalformatting-fieldid"></a>
The field ID of the cell for conditional formatting\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-quicksight-analysis-pivottablecellconditionalformatting-scope"></a>
The scope of the cell for conditional formatting\.  
*Required*: No  
*Type*: [PivotTableConditionalFormattingScope](aws-properties-quicksight-analysis-pivottableconditionalformattingscope.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scopes`  <a name="cfn-quicksight-analysis-pivottablecellconditionalformatting-scopes"></a>
A list of cell scopes for conditional formatting\.  
*Required*: No  
*Type*: List of [PivotTableConditionalFormattingScope](aws-properties-quicksight-analysis-pivottableconditionalformattingscope.md)  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextFormat`  <a name="cfn-quicksight-analysis-pivottablecellconditionalformatting-textformat"></a>
The text format of the cell for conditional formatting\.  
*Required*: No  
*Type*: [TextConditionalFormat](aws-properties-quicksight-analysis-textconditionalformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)