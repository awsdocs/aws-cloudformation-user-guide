# AWS::QuickSight::Dashboard FieldBasedTooltip<a name="aws-properties-quicksight-dashboard-fieldbasedtooltip"></a>

The setup for the detailed tooltip\.

## Syntax<a name="aws-properties-quicksight-dashboard-fieldbasedtooltip-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-fieldbasedtooltip-syntax.json"></a>

```
{
  "[AggregationVisibility](#cfn-quicksight-dashboard-fieldbasedtooltip-aggregationvisibility)" : String,
  "[TooltipFields](#cfn-quicksight-dashboard-fieldbasedtooltip-tooltipfields)" : [ TooltipItem, ... ],
  "[TooltipTitleType](#cfn-quicksight-dashboard-fieldbasedtooltip-tooltiptitletype)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-fieldbasedtooltip-syntax.yaml"></a>

```
  [AggregationVisibility](#cfn-quicksight-dashboard-fieldbasedtooltip-aggregationvisibility): String
  [TooltipFields](#cfn-quicksight-dashboard-fieldbasedtooltip-tooltipfields): 
    - TooltipItem
  [TooltipTitleType](#cfn-quicksight-dashboard-fieldbasedtooltip-tooltiptitletype): String
```

## Properties<a name="aws-properties-quicksight-dashboard-fieldbasedtooltip-properties"></a>

`AggregationVisibility`  <a name="cfn-quicksight-dashboard-fieldbasedtooltip-aggregationvisibility"></a>
The visibility of `Show aggregations`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TooltipFields`  <a name="cfn-quicksight-dashboard-fieldbasedtooltip-tooltipfields"></a>
The fields configuration in the tooltip\.  
*Required*: No  
*Type*: List of [TooltipItem](aws-properties-quicksight-dashboard-tooltipitem.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TooltipTitleType`  <a name="cfn-quicksight-dashboard-fieldbasedtooltip-tooltiptitletype"></a>
The type for the >tooltip title\. Choose one of the following options:  
+  `NONE`: Doesn't use the primary value as the title\.
+  `PRIMARY_VALUE`: Uses primary value as the title\.
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | PRIMARY_VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)