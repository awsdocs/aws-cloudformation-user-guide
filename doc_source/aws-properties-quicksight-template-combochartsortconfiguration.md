# AWS::QuickSight::Template ComboChartSortConfiguration<a name="aws-properties-quicksight-template-combochartsortconfiguration"></a>

The sort configuration of a `ComboChartVisual`\.

## Syntax<a name="aws-properties-quicksight-template-combochartsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-combochartsortconfiguration-syntax.json"></a>

```
{
  "[CategoryItemsLimit](#cfn-quicksight-template-combochartsortconfiguration-categoryitemslimit)" : ItemsLimitConfiguration,
  "[CategorySort](#cfn-quicksight-template-combochartsortconfiguration-categorysort)" : [ FieldSortOptions, ... ],
  "[ColorItemsLimit](#cfn-quicksight-template-combochartsortconfiguration-coloritemslimit)" : ItemsLimitConfiguration,
  "[ColorSort](#cfn-quicksight-template-combochartsortconfiguration-colorsort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-combochartsortconfiguration-syntax.yaml"></a>

```
  [CategoryItemsLimit](#cfn-quicksight-template-combochartsortconfiguration-categoryitemslimit): 
    ItemsLimitConfiguration
  [CategorySort](#cfn-quicksight-template-combochartsortconfiguration-categorysort): 
    - FieldSortOptions
  [ColorItemsLimit](#cfn-quicksight-template-combochartsortconfiguration-coloritemslimit): 
    ItemsLimitConfiguration
  [ColorSort](#cfn-quicksight-template-combochartsortconfiguration-colorsort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-template-combochartsortconfiguration-properties"></a>

`CategoryItemsLimit`  <a name="cfn-quicksight-template-combochartsortconfiguration-categoryitemslimit"></a>
The item limit configuration for the category field well of a combo chart\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-template-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategorySort`  <a name="cfn-quicksight-template-combochartsortconfiguration-categorysort"></a>
The sort configuration of the category field well in a combo chart\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-template-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorItemsLimit`  <a name="cfn-quicksight-template-combochartsortconfiguration-coloritemslimit"></a>
The item limit configuration of the color field well in a combo chart\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-template-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorSort`  <a name="cfn-quicksight-template-combochartsortconfiguration-colorsort"></a>
The sort configuration of the color field well in a combo chart\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-template-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)