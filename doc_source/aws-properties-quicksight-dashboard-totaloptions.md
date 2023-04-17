# AWS::QuickSight::Dashboard TotalOptions<a name="aws-properties-quicksight-dashboard-totaloptions"></a>

The total options for a table visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-totaloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-totaloptions-syntax.json"></a>

```
{
  "[CustomLabel](#cfn-quicksight-dashboard-totaloptions-customlabel)" : String,
  "[Placement](#cfn-quicksight-dashboard-totaloptions-placement)" : String,
  "[ScrollStatus](#cfn-quicksight-dashboard-totaloptions-scrollstatus)" : String,
  "[TotalCellStyle](#cfn-quicksight-dashboard-totaloptions-totalcellstyle)" : TableCellStyle,
  "[TotalsVisibility](#cfn-quicksight-dashboard-totaloptions-totalsvisibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-totaloptions-syntax.yaml"></a>

```
  [CustomLabel](#cfn-quicksight-dashboard-totaloptions-customlabel): String
  [Placement](#cfn-quicksight-dashboard-totaloptions-placement): String
  [ScrollStatus](#cfn-quicksight-dashboard-totaloptions-scrollstatus): String
  [TotalCellStyle](#cfn-quicksight-dashboard-totaloptions-totalcellstyle): 
    TableCellStyle
  [TotalsVisibility](#cfn-quicksight-dashboard-totaloptions-totalsvisibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-totaloptions-properties"></a>

`CustomLabel`  <a name="cfn-quicksight-dashboard-totaloptions-customlabel"></a>
The custom label string for the total cells\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Placement`  <a name="cfn-quicksight-dashboard-totaloptions-placement"></a>
The placement \(start, end\) for the total cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `END | START`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScrollStatus`  <a name="cfn-quicksight-dashboard-totaloptions-scrollstatus"></a>
The scroll status \(pinned, scrolled\) for the total cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PINNED | SCROLLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalCellStyle`  <a name="cfn-quicksight-dashboard-totaloptions-totalcellstyle"></a>
Cell styling options for the total cells\.  
*Required*: No  
*Type*: [TableCellStyle](aws-properties-quicksight-dashboard-tablecellstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalsVisibility`  <a name="cfn-quicksight-dashboard-totaloptions-totalsvisibility"></a>
The visibility configuration for the total cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)