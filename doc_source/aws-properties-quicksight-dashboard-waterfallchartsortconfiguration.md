# AWS::QuickSight::Dashboard WaterfallChartSortConfiguration<a name="aws-properties-quicksight-dashboard-waterfallchartsortconfiguration"></a>

The sort configuration of a waterfall visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-waterfallchartsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-waterfallchartsortconfiguration-syntax.json"></a>

```
{
  "[BreakdownItemsLimit](#cfn-quicksight-dashboard-waterfallchartsortconfiguration-breakdownitemslimit)" : ItemsLimitConfiguration,
  "[CategorySort](#cfn-quicksight-dashboard-waterfallchartsortconfiguration-categorysort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-waterfallchartsortconfiguration-syntax.yaml"></a>

```
  [BreakdownItemsLimit](#cfn-quicksight-dashboard-waterfallchartsortconfiguration-breakdownitemslimit): 
    ItemsLimitConfiguration
  [CategorySort](#cfn-quicksight-dashboard-waterfallchartsortconfiguration-categorysort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-waterfallchartsortconfiguration-properties"></a>

`BreakdownItemsLimit`  <a name="cfn-quicksight-dashboard-waterfallchartsortconfiguration-breakdownitemslimit"></a>
The limit on the number of bar groups that are displayed\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-dashboard-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategorySort`  <a name="cfn-quicksight-dashboard-waterfallchartsortconfiguration-categorysort"></a>
The sort configuration of the category fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-dashboard-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)