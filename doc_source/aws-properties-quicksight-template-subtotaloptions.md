# AWS::QuickSight::Template SubtotalOptions<a name="aws-properties-quicksight-template-subtotaloptions"></a>

The subtotal options\.

## Syntax<a name="aws-properties-quicksight-template-subtotaloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-subtotaloptions-syntax.json"></a>

```
{
  "[CustomLabel](#cfn-quicksight-template-subtotaloptions-customlabel)" : String,
  "[FieldLevel](#cfn-quicksight-template-subtotaloptions-fieldlevel)" : String,
  "[FieldLevelOptions](#cfn-quicksight-template-subtotaloptions-fieldleveloptions)" : [ PivotTableFieldSubtotalOptions, ... ],
  "[MetricHeaderCellStyle](#cfn-quicksight-template-subtotaloptions-metricheadercellstyle)" : TableCellStyle,
  "[TotalCellStyle](#cfn-quicksight-template-subtotaloptions-totalcellstyle)" : TableCellStyle,
  "[TotalsVisibility](#cfn-quicksight-template-subtotaloptions-totalsvisibility)" : String,
  "[ValueCellStyle](#cfn-quicksight-template-subtotaloptions-valuecellstyle)" : TableCellStyle
}
```

### YAML<a name="aws-properties-quicksight-template-subtotaloptions-syntax.yaml"></a>

```
  [CustomLabel](#cfn-quicksight-template-subtotaloptions-customlabel): String
  [FieldLevel](#cfn-quicksight-template-subtotaloptions-fieldlevel): String
  [FieldLevelOptions](#cfn-quicksight-template-subtotaloptions-fieldleveloptions): 
    - PivotTableFieldSubtotalOptions
  [MetricHeaderCellStyle](#cfn-quicksight-template-subtotaloptions-metricheadercellstyle): 
    TableCellStyle
  [TotalCellStyle](#cfn-quicksight-template-subtotaloptions-totalcellstyle): 
    TableCellStyle
  [TotalsVisibility](#cfn-quicksight-template-subtotaloptions-totalsvisibility): String
  [ValueCellStyle](#cfn-quicksight-template-subtotaloptions-valuecellstyle): 
    TableCellStyle
```

## Properties<a name="aws-properties-quicksight-template-subtotaloptions-properties"></a>

`CustomLabel`  <a name="cfn-quicksight-template-subtotaloptions-customlabel"></a>
The custom label string for the subtotal cells\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldLevel`  <a name="cfn-quicksight-template-subtotaloptions-fieldlevel"></a>
The field level \(all, custom, last\) for the subtotal cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ALL | CUSTOM | LAST`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldLevelOptions`  <a name="cfn-quicksight-template-subtotaloptions-fieldleveloptions"></a>
The optional configuration of subtotal cells\.  
*Required*: No  
*Type*: List of [PivotTableFieldSubtotalOptions](aws-properties-quicksight-template-pivottablefieldsubtotaloptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricHeaderCellStyle`  <a name="cfn-quicksight-template-subtotaloptions-metricheadercellstyle"></a>
The cell styling options for the subtotals of header cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalCellStyle`  <a name="cfn-quicksight-template-subtotaloptions-totalcellstyle"></a>
The cell styling options for the subtotal cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalsVisibility`  <a name="cfn-quicksight-template-subtotaloptions-totalsvisibility"></a>
The visibility configuration for the subtotal cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueCellStyle`  <a name="cfn-quicksight-template-subtotaloptions-valuecellstyle"></a>
The cell styling options for the subtotals of value cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-template-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)