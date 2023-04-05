# AWS::QuickSight::Template TableOptions<a name="aws-properties-quicksight-template-tableoptions"></a>

The table options for a table visual\.

## Syntax<a name="aws-properties-quicksight-template-tableoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tableoptions-syntax.json"></a>

```
{
  "[CellStyle](#cfn-quicksight-template-tableoptions-cellstyle)" : TableCellStyle,
  "[HeaderStyle](#cfn-quicksight-template-tableoptions-headerstyle)" : TableCellStyle,
  "[Orientation](#cfn-quicksight-template-tableoptions-orientation)" : String,
  "[RowAlternateColorOptions](#cfn-quicksight-template-tableoptions-rowalternatecoloroptions)" : RowAlternateColorOptions
}
```

### YAML<a name="aws-properties-quicksight-template-tableoptions-syntax.yaml"></a>

```
  [CellStyle](#cfn-quicksight-template-tableoptions-cellstyle): 
    TableCellStyle
  [HeaderStyle](#cfn-quicksight-template-tableoptions-headerstyle): 
    TableCellStyle
  [Orientation](#cfn-quicksight-template-tableoptions-orientation): String
  [RowAlternateColorOptions](#cfn-quicksight-template-tableoptions-rowalternatecoloroptions): 
    RowAlternateColorOptions
```

## Properties<a name="aws-properties-quicksight-template-tableoptions-properties"></a>

`CellStyle`  <a name="cfn-quicksight-template-tableoptions-cellstyle"></a>
The table cell style of table cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderStyle`  <a name="cfn-quicksight-template-tableoptions-headerstyle"></a>
The table cell style of a table header\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Orientation`  <a name="cfn-quicksight-template-tableoptions-orientation"></a>
The orientation \(vertical, horizontal\) for a table\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HORIZONTAL | VERTICAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowAlternateColorOptions`  <a name="cfn-quicksight-template-tableoptions-rowalternatecoloroptions"></a>
The row alternate color options \(widget status, row alternate colors\) for a table\.  
*Required*: No  
*Type*: [RowAlternateColorOptions](aws-properties-quicksight-template-rowalternatecoloroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)