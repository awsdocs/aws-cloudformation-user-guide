# AWS::QuickSight::Analysis TableOptions<a name="aws-properties-quicksight-analysis-tableoptions"></a>

The table options for a table visual\.

## Syntax<a name="aws-properties-quicksight-analysis-tableoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tableoptions-syntax.json"></a>

```
{
  "[CellStyle](#cfn-quicksight-analysis-tableoptions-cellstyle)" : TableCellStyle,
  "[HeaderStyle](#cfn-quicksight-analysis-tableoptions-headerstyle)" : TableCellStyle,
  "[Orientation](#cfn-quicksight-analysis-tableoptions-orientation)" : String,
  "[RowAlternateColorOptions](#cfn-quicksight-analysis-tableoptions-rowalternatecoloroptions)" : RowAlternateColorOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-tableoptions-syntax.yaml"></a>

```
  [CellStyle](#cfn-quicksight-analysis-tableoptions-cellstyle): 
    TableCellStyle
  [HeaderStyle](#cfn-quicksight-analysis-tableoptions-headerstyle): 
    TableCellStyle
  [Orientation](#cfn-quicksight-analysis-tableoptions-orientation): String
  [RowAlternateColorOptions](#cfn-quicksight-analysis-tableoptions-rowalternatecoloroptions): 
    RowAlternateColorOptions
```

## Properties<a name="aws-properties-quicksight-analysis-tableoptions-properties"></a>

`CellStyle`  <a name="cfn-quicksight-analysis-tableoptions-cellstyle"></a>
The table cell style of table cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderStyle`  <a name="cfn-quicksight-analysis-tableoptions-headerstyle"></a>
The table cell style of a table header\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Orientation`  <a name="cfn-quicksight-analysis-tableoptions-orientation"></a>
The orientation \(vertical, horizontal\) for a table\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HORIZONTAL | VERTICAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowAlternateColorOptions`  <a name="cfn-quicksight-analysis-tableoptions-rowalternatecoloroptions"></a>
The row alternate color options \(widget status, row alternate colors\) for a table\.  
*Required*: No  
*Type*: [RowAlternateColorOptions](aws-properties-quicksight-analysis-rowalternatecoloroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)