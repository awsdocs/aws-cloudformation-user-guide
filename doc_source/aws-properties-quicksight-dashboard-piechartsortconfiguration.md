# AWS::QuickSight::Dashboard PieChartSortConfiguration<a name="aws-properties-quicksight-dashboard-piechartsortconfiguration"></a>

The sort configuration of a pie chart\.

## Syntax<a name="aws-properties-quicksight-dashboard-piechartsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-piechartsortconfiguration-syntax.json"></a>

```
{
  "[CategoryItemsLimit](#cfn-quicksight-dashboard-piechartsortconfiguration-categoryitemslimit)" : ItemsLimitConfiguration,
  "[CategorySort](#cfn-quicksight-dashboard-piechartsortconfiguration-categorysort)" : [ FieldSortOptions, ... ],
  "[SmallMultiplesLimitConfiguration](#cfn-quicksight-dashboard-piechartsortconfiguration-smallmultipleslimitconfiguration)" : ItemsLimitConfiguration,
  "[SmallMultiplesSort](#cfn-quicksight-dashboard-piechartsortconfiguration-smallmultiplessort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-piechartsortconfiguration-syntax.yaml"></a>

```
  [CategoryItemsLimit](#cfn-quicksight-dashboard-piechartsortconfiguration-categoryitemslimit): 
    ItemsLimitConfiguration
  [CategorySort](#cfn-quicksight-dashboard-piechartsortconfiguration-categorysort): 
    - FieldSortOptions
  [SmallMultiplesLimitConfiguration](#cfn-quicksight-dashboard-piechartsortconfiguration-smallmultipleslimitconfiguration): 
    ItemsLimitConfiguration
  [SmallMultiplesSort](#cfn-quicksight-dashboard-piechartsortconfiguration-smallmultiplessort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-piechartsortconfiguration-properties"></a>

`CategoryItemsLimit`  <a name="cfn-quicksight-dashboard-piechartsortconfiguration-categoryitemslimit"></a>
The limit on the number of categories that are displayed in a pie chart\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-dashboard-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategorySort`  <a name="cfn-quicksight-dashboard-piechartsortconfiguration-categorysort"></a>
The sort configuration of the category fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-dashboard-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesLimitConfiguration`  <a name="cfn-quicksight-dashboard-piechartsortconfiguration-smallmultipleslimitconfiguration"></a>
The limit on the number of small multiples panels that are displayed\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-dashboard-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesSort`  <a name="cfn-quicksight-dashboard-piechartsortconfiguration-smallmultiplessort"></a>
The sort configuration of the small multiples field\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-dashboard-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)