# AWS::QuickSight::Analysis TooltipItem<a name="aws-properties-quicksight-analysis-tooltipitem"></a>

The tooltip\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-tooltipitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tooltipitem-syntax.json"></a>

```
{
  "[ColumnTooltipItem](#cfn-quicksight-analysis-tooltipitem-columntooltipitem)" : ColumnTooltipItem,
  "[FieldTooltipItem](#cfn-quicksight-analysis-tooltipitem-fieldtooltipitem)" : FieldTooltipItem
}
```

### YAML<a name="aws-properties-quicksight-analysis-tooltipitem-syntax.yaml"></a>

```
  [ColumnTooltipItem](#cfn-quicksight-analysis-tooltipitem-columntooltipitem): 
    ColumnTooltipItem
  [FieldTooltipItem](#cfn-quicksight-analysis-tooltipitem-fieldtooltipitem): 
    FieldTooltipItem
```

## Properties<a name="aws-properties-quicksight-analysis-tooltipitem-properties"></a>

`ColumnTooltipItem`  <a name="cfn-quicksight-analysis-tooltipitem-columntooltipitem"></a>
The tooltip item for the columns that are not part of a field well\.  
*Required*: No  
*Type*: [ColumnTooltipItem](aws-properties-quicksight-analysis-columntooltipitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldTooltipItem`  <a name="cfn-quicksight-analysis-tooltipitem-fieldtooltipitem"></a>
The tooltip item for the fields\.  
*Required*: No  
*Type*: [FieldTooltipItem](aws-properties-quicksight-analysis-fieldtooltipitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)