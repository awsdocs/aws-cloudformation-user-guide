# AWS::QuickSight::Dashboard PivotTableConditionalFormattingOption<a name="aws-properties-quicksight-dashboard-pivottableconditionalformattingoption"></a>

Conditional formatting options for a `PivotTableVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-pivottableconditionalformattingoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-pivottableconditionalformattingoption-syntax.json"></a>

```
{
  "[Cell](#cfn-quicksight-dashboard-pivottableconditionalformattingoption-cell)" : PivotTableCellConditionalFormatting
}
```

### YAML<a name="aws-properties-quicksight-dashboard-pivottableconditionalformattingoption-syntax.yaml"></a>

```
  [Cell](#cfn-quicksight-dashboard-pivottableconditionalformattingoption-cell): 
    PivotTableCellConditionalFormatting
```

## Properties<a name="aws-properties-quicksight-dashboard-pivottableconditionalformattingoption-properties"></a>

`Cell`  <a name="cfn-quicksight-dashboard-pivottableconditionalformattingoption-cell"></a>
The cell conditional formatting option for a pivot table\.  
*Required*: No  
*Type*: [PivotTableCellConditionalFormatting](aws-properties-quicksight-dashboard-pivottablecellconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)