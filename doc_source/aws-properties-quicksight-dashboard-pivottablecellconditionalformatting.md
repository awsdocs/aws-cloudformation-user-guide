# AWS::QuickSight::Dashboard PivotTableCellConditionalFormatting<a name="aws-properties-quicksight-dashboard-pivottablecellconditionalformatting"></a>

The cell conditional formatting option for a pivot table\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottablecellconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottablecellconditionalformatting-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-dashboard-pivottablecellconditionalformatting-fieldid)" : String,
  "[Scope](#cfn-quicksight-dashboard-pivottablecellconditionalformatting-scope)" : PivotTableConditionalFormattingScope,
  "[TextFormat](#cfn-quicksight-dashboard-pivottablecellconditionalformatting-textformat)" : TextConditionalFormat
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottablecellconditionalformatting-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-dashboard-pivottablecellconditionalformatting-fieldid): String
  [Scope](#cfn-quicksight-dashboard-pivottablecellconditionalformatting-scope): 
    PivotTableConditionalFormattingScope
  [TextFormat](#cfn-quicksight-dashboard-pivottablecellconditionalformatting-textformat): 
    TextConditionalFormat
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottablecellconditionalformatting-properties"></a>

`FieldId`  <a name="cfn-quicksight-dashboard-pivottablecellconditionalformatting-fieldid"></a>
The field ID of the cell for conditional formatting\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-quicksight-dashboard-pivottablecellconditionalformatting-scope"></a>
The scope of the cell for conditional formatting\.  
*Required*: No  
*Type*: [PivotTableConditionalFormattingScope](aws-properties-quicksight-dashboard-pivottableconditionalformattingscope.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextFormat`  <a name="cfn-quicksight-dashboard-pivottablecellconditionalformatting-textformat"></a>
The text format of the cell for conditional formatting\.  
*Required*: No  
*Type*: [TextConditionalFormat](aws-properties-quicksight-dashboard-textconditionalformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)