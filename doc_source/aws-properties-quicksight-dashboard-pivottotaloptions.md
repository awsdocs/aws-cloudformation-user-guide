# AWS::QuickSight::Dashboard PivotTotalOptions<a name="aws-properties-quicksight-dashboard-pivottotaloptions"></a>

The optional configuration of totals cells in a `PivotTableVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottotaloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottotaloptions-syntax.json"></a>

```
{
  "[CustomLabel](#cfn-quicksight-dashboard-pivottotaloptions-customlabel)" : String,
  "[MetricHeaderCellStyle](#cfn-quicksight-dashboard-pivottotaloptions-metricheadercellstyle)" : TableCellStyle,
  "[Placement](#cfn-quicksight-dashboard-pivottotaloptions-placement)" : String,
  "[ScrollStatus](#cfn-quicksight-dashboard-pivottotaloptions-scrollstatus)" : String,
  "[TotalCellStyle](#cfn-quicksight-dashboard-pivottotaloptions-totalcellstyle)" : TableCellStyle,
  "[TotalsVisibility](#cfn-quicksight-dashboard-pivottotaloptions-totalsvisibility)" : String,
  "[ValueCellStyle](#cfn-quicksight-dashboard-pivottotaloptions-valuecellstyle)" : TableCellStyle
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottotaloptions-syntax.yaml"></a>

```
  [CustomLabel](#cfn-quicksight-dashboard-pivottotaloptions-customlabel): String
  [MetricHeaderCellStyle](#cfn-quicksight-dashboard-pivottotaloptions-metricheadercellstyle): 
    TableCellStyle
  [Placement](#cfn-quicksight-dashboard-pivottotaloptions-placement): String
  [ScrollStatus](#cfn-quicksight-dashboard-pivottotaloptions-scrollstatus): String
  [TotalCellStyle](#cfn-quicksight-dashboard-pivottotaloptions-totalcellstyle): 
    TableCellStyle
  [TotalsVisibility](#cfn-quicksight-dashboard-pivottotaloptions-totalsvisibility): String
  [ValueCellStyle](#cfn-quicksight-dashboard-pivottotaloptions-valuecellstyle): 
    TableCellStyle
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottotaloptions-properties"></a>

`CustomLabel`  <a name="cfn-quicksight-dashboard-pivottotaloptions-customlabel"></a>
The custom label string for the total cells\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricHeaderCellStyle`  <a name="cfn-quicksight-dashboard-pivottotaloptions-metricheadercellstyle"></a>
The cell styling options for the total of header cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-dashboard-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Placement`  <a name="cfn-quicksight-dashboard-pivottotaloptions-placement"></a>
The placement \(start, end\) for the total cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `END | START`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScrollStatus`  <a name="cfn-quicksight-dashboard-pivottotaloptions-scrollstatus"></a>
The scroll status \(pinned, scrolled\) for the total cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PINNED | SCROLLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalCellStyle`  <a name="cfn-quicksight-dashboard-pivottotaloptions-totalcellstyle"></a>
The cell styling options for the total cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-dashboard-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalsVisibility`  <a name="cfn-quicksight-dashboard-pivottotaloptions-totalsvisibility"></a>
The visibility configuration for the total cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueCellStyle`  <a name="cfn-quicksight-dashboard-pivottotaloptions-valuecellstyle"></a>
The cell styling options for the totals of value cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-dashboard-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)