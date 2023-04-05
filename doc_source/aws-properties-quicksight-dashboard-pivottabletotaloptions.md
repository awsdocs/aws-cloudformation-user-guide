# AWS::QuickSight::Dashboard PivotTableTotalOptions<a name="aws-properties-quicksight-dashboard-pivottabletotaloptions"></a>

The total options for a pivot table visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottabletotaloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottabletotaloptions-syntax.json"></a>

```
{
  "[ColumnSubtotalOptions](#cfn-quicksight-dashboard-pivottabletotaloptions-columnsubtotaloptions)" : SubtotalOptions,
  "[ColumnTotalOptions](#cfn-quicksight-dashboard-pivottabletotaloptions-columntotaloptions)" : PivotTotalOptions,
  "[RowSubtotalOptions](#cfn-quicksight-dashboard-pivottabletotaloptions-rowsubtotaloptions)" : SubtotalOptions,
  "[RowTotalOptions](#cfn-quicksight-dashboard-pivottabletotaloptions-rowtotaloptions)" : PivotTotalOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottabletotaloptions-syntax.yaml"></a>

```
  [ColumnSubtotalOptions](#cfn-quicksight-dashboard-pivottabletotaloptions-columnsubtotaloptions): 
    SubtotalOptions
  [ColumnTotalOptions](#cfn-quicksight-dashboard-pivottabletotaloptions-columntotaloptions): 
    PivotTotalOptions
  [RowSubtotalOptions](#cfn-quicksight-dashboard-pivottabletotaloptions-rowsubtotaloptions): 
    SubtotalOptions
  [RowTotalOptions](#cfn-quicksight-dashboard-pivottabletotaloptions-rowtotaloptions): 
    PivotTotalOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottabletotaloptions-properties"></a>

`ColumnSubtotalOptions`  <a name="cfn-quicksight-dashboard-pivottabletotaloptions-columnsubtotaloptions"></a>
The column subtotal options\.  
*Required*: No  
*Type*: [SubtotalOptions](aws-properties-quicksight-dashboard-subtotaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnTotalOptions`  <a name="cfn-quicksight-dashboard-pivottabletotaloptions-columntotaloptions"></a>
The column total options\.  
*Required*: No  
*Type*: [PivotTotalOptions](aws-properties-quicksight-dashboard-pivottotaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowSubtotalOptions`  <a name="cfn-quicksight-dashboard-pivottabletotaloptions-rowsubtotaloptions"></a>
The row subtotal options\.  
*Required*: No  
*Type*: [SubtotalOptions](aws-properties-quicksight-dashboard-subtotaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RowTotalOptions`  <a name="cfn-quicksight-dashboard-pivottabletotaloptions-rowtotaloptions"></a>
The row total options\.  
*Required*: No  
*Type*: [PivotTotalOptions](aws-properties-quicksight-dashboard-pivottotaloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)