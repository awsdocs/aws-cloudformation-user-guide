# AWS::QuickSight::Dashboard TableCellConditionalFormatting<a name="aws-properties-quicksight-dashboard-tablecellconditionalformatting"></a>

The cell conditional formatting option for a table\.

## Syntax<a name="aws-properties-quicksight-dashboard-tablecellconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tablecellconditionalformatting-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-dashboard-tablecellconditionalformatting-fieldid)" : String,
  "[TextFormat](#cfn-quicksight-dashboard-tablecellconditionalformatting-textformat)" : TextConditionalFormat
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tablecellconditionalformatting-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-dashboard-tablecellconditionalformatting-fieldid): String
  [TextFormat](#cfn-quicksight-dashboard-tablecellconditionalformatting-textformat): 
    TextConditionalFormat
```

## Properties<a name="aws-properties-quicksight-dashboard-tablecellconditionalformatting-properties"></a>

`FieldId`  <a name="cfn-quicksight-dashboard-tablecellconditionalformatting-fieldid"></a>
The field ID of the cell for conditional formatting\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextFormat`  <a name="cfn-quicksight-dashboard-tablecellconditionalformatting-textformat"></a>
The text format of the cell for conditional formatting\.  
*Required*: No  
*Type*: [TextConditionalFormat](aws-properties-quicksight-dashboard-textconditionalformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)