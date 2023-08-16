# AWS::QuickSight::Template LineChartSortConfiguration<a name="aws-properties-quicksight-template-linechartsortconfiguration"></a>

The sort configuration of a line chart\.

## Syntax<a name="aws-properties-quicksight-template-linechartsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-linechartsortconfiguration-syntax.json"></a>

```
{
  "[CategoryItemsLimitConfiguration](#cfn-quicksight-template-linechartsortconfiguration-categoryitemslimitconfiguration)" : ItemsLimitConfiguration,
  "[CategorySort](#cfn-quicksight-template-linechartsortconfiguration-categorysort)" : [ FieldSortOptions, ... ],
  "[ColorItemsLimitConfiguration](#cfn-quicksight-template-linechartsortconfiguration-coloritemslimitconfiguration)" : ItemsLimitConfiguration,
  "[SmallMultiplesLimitConfiguration](#cfn-quicksight-template-linechartsortconfiguration-smallmultipleslimitconfiguration)" : ItemsLimitConfiguration,
  "[SmallMultiplesSort](#cfn-quicksight-template-linechartsortconfiguration-smallmultiplessort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-linechartsortconfiguration-syntax.yaml"></a>

```
  [CategoryItemsLimitConfiguration](#cfn-quicksight-template-linechartsortconfiguration-categoryitemslimitconfiguration): 
    ItemsLimitConfiguration
  [CategorySort](#cfn-quicksight-template-linechartsortconfiguration-categorysort): 
    - FieldSortOptions
  [ColorItemsLimitConfiguration](#cfn-quicksight-template-linechartsortconfiguration-coloritemslimitconfiguration): 
    ItemsLimitConfiguration
  [SmallMultiplesLimitConfiguration](#cfn-quicksight-template-linechartsortconfiguration-smallmultipleslimitconfiguration): 
    ItemsLimitConfiguration
  [SmallMultiplesSort](#cfn-quicksight-template-linechartsortconfiguration-smallmultiplessort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-template-linechartsortconfiguration-properties"></a>

`CategoryItemsLimitConfiguration`  <a name="cfn-quicksight-template-linechartsortconfiguration-categoryitemslimitconfiguration"></a>
The limit on the number of categories that are displayed in a line chart\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-template-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategorySort`  <a name="cfn-quicksight-template-linechartsortconfiguration-categorysort"></a>
The sort configuration of the category fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-template-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorItemsLimitConfiguration`  <a name="cfn-quicksight-template-linechartsortconfiguration-coloritemslimitconfiguration"></a>
The limit on the number of lines that are displayed in a line chart\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-template-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesLimitConfiguration`  <a name="cfn-quicksight-template-linechartsortconfiguration-smallmultipleslimitconfiguration"></a>
The limit on the number of small multiples panels that are displayed\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-template-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesSort`  <a name="cfn-quicksight-template-linechartsortconfiguration-smallmultiplessort"></a>
The sort configuration of the small multiples field\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-template-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)