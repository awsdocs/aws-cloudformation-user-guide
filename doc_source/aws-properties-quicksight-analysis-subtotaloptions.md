# AWS::QuickSight::Analysis SubtotalOptions<a name="aws-properties-quicksight-analysis-subtotaloptions"></a>

The subtotal options\.

## Syntax<a name="aws-properties-quicksight-analysis-subtotaloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-subtotaloptions-syntax.json"></a>

```
{
  "[CustomLabel](#cfn-quicksight-analysis-subtotaloptions-customlabel)" : String,
  "[FieldLevel](#cfn-quicksight-analysis-subtotaloptions-fieldlevel)" : String,
  "[FieldLevelOptions](#cfn-quicksight-analysis-subtotaloptions-fieldleveloptions)" : [ PivotTableFieldSubtotalOptions, ... ],
  "[MetricHeaderCellStyle](#cfn-quicksight-analysis-subtotaloptions-metricheadercellstyle)" : TableCellStyle,
  "[StyleTargets](#cfn-quicksight-analysis-subtotaloptions-styletargets)" : [ TableStyleTarget, ... ],
  "[TotalCellStyle](#cfn-quicksight-analysis-subtotaloptions-totalcellstyle)" : TableCellStyle,
  "[TotalsVisibility](#cfn-quicksight-analysis-subtotaloptions-totalsvisibility)" : String,
  "[ValueCellStyle](#cfn-quicksight-analysis-subtotaloptions-valuecellstyle)" : TableCellStyle
}
```

### YAML<a name="aws-properties-quicksight-analysis-subtotaloptions-syntax.yaml"></a>

```
  [CustomLabel](#cfn-quicksight-analysis-subtotaloptions-customlabel): String
  [FieldLevel](#cfn-quicksight-analysis-subtotaloptions-fieldlevel): String
  [FieldLevelOptions](#cfn-quicksight-analysis-subtotaloptions-fieldleveloptions): 
    - PivotTableFieldSubtotalOptions
  [MetricHeaderCellStyle](#cfn-quicksight-analysis-subtotaloptions-metricheadercellstyle): 
    TableCellStyle
  [StyleTargets](#cfn-quicksight-analysis-subtotaloptions-styletargets): 
    - TableStyleTarget
  [TotalCellStyle](#cfn-quicksight-analysis-subtotaloptions-totalcellstyle): 
    TableCellStyle
  [TotalsVisibility](#cfn-quicksight-analysis-subtotaloptions-totalsvisibility): String
  [ValueCellStyle](#cfn-quicksight-analysis-subtotaloptions-valuecellstyle): 
    TableCellStyle
```

## Properties<a name="aws-properties-quicksight-analysis-subtotaloptions-properties"></a>

`CustomLabel`  <a name="cfn-quicksight-analysis-subtotaloptions-customlabel"></a>
The custom label string for the subtotal cells\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldLevel`  <a name="cfn-quicksight-analysis-subtotaloptions-fieldlevel"></a>
The field level \(all, custom, last\) for the subtotal cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ALL | CUSTOM | LAST`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldLevelOptions`  <a name="cfn-quicksight-analysis-subtotaloptions-fieldleveloptions"></a>
The optional configuration of subtotal cells\.  
*Required*: No  
*Type*: List of [PivotTableFieldSubtotalOptions](aws-properties-quicksight-analysis-pivottablefieldsubtotaloptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricHeaderCellStyle`  <a name="cfn-quicksight-analysis-subtotaloptions-metricheadercellstyle"></a>
The cell styling options for the subtotals of header cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StyleTargets`  <a name="cfn-quicksight-analysis-subtotaloptions-styletargets"></a>
The style targets options for subtotals\.  
*Required*: No  
*Type*: List of [TableStyleTarget](aws-properties-quicksight-analysis-tablestyletarget.md)  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalCellStyle`  <a name="cfn-quicksight-analysis-subtotaloptions-totalcellstyle"></a>
The cell styling options for the subtotal cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalsVisibility`  <a name="cfn-quicksight-analysis-subtotaloptions-totalsvisibility"></a>
The visibility configuration for the subtotal cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueCellStyle`  <a name="cfn-quicksight-analysis-subtotaloptions-valuecellstyle"></a>
The cell styling options for the subtotals of value cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-analysis-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)