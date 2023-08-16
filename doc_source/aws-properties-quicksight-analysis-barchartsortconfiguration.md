# AWS::QuickSight::Analysis BarChartSortConfiguration<a name="aws-properties-quicksight-analysis-barchartsortconfiguration"></a>

sort\-configuration\-description

## Syntax<a name="aws-properties-quicksight-analysis-barchartsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-barchartsortconfiguration-syntax.json"></a>

```
{
  "[CategoryItemsLimit](#cfn-quicksight-analysis-barchartsortconfiguration-categoryitemslimit)" : ItemsLimitConfiguration,
  "[CategorySort](#cfn-quicksight-analysis-barchartsortconfiguration-categorysort)" : [ FieldSortOptions, ... ],
  "[ColorItemsLimit](#cfn-quicksight-analysis-barchartsortconfiguration-coloritemslimit)" : ItemsLimitConfiguration,
  "[ColorSort](#cfn-quicksight-analysis-barchartsortconfiguration-colorsort)" : [ FieldSortOptions, ... ],
  "[SmallMultiplesLimitConfiguration](#cfn-quicksight-analysis-barchartsortconfiguration-smallmultipleslimitconfiguration)" : ItemsLimitConfiguration,
  "[SmallMultiplesSort](#cfn-quicksight-analysis-barchartsortconfiguration-smallmultiplessort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-barchartsortconfiguration-syntax.yaml"></a>

```
  [CategoryItemsLimit](#cfn-quicksight-analysis-barchartsortconfiguration-categoryitemslimit): 
    ItemsLimitConfiguration
  [CategorySort](#cfn-quicksight-analysis-barchartsortconfiguration-categorysort): 
    - FieldSortOptions
  [ColorItemsLimit](#cfn-quicksight-analysis-barchartsortconfiguration-coloritemslimit): 
    ItemsLimitConfiguration
  [ColorSort](#cfn-quicksight-analysis-barchartsortconfiguration-colorsort): 
    - FieldSortOptions
  [SmallMultiplesLimitConfiguration](#cfn-quicksight-analysis-barchartsortconfiguration-smallmultipleslimitconfiguration): 
    ItemsLimitConfiguration
  [SmallMultiplesSort](#cfn-quicksight-analysis-barchartsortconfiguration-smallmultiplessort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-analysis-barchartsortconfiguration-properties"></a>

`CategoryItemsLimit`  <a name="cfn-quicksight-analysis-barchartsortconfiguration-categoryitemslimit"></a>
The limit on the number of categories displayed in a bar chart\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-analysis-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategorySort`  <a name="cfn-quicksight-analysis-barchartsortconfiguration-categorysort"></a>
The sort configuration of category fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-analysis-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorItemsLimit`  <a name="cfn-quicksight-analysis-barchartsortconfiguration-coloritemslimit"></a>
The limit on the number of values displayed in a bar chart\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-analysis-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColorSort`  <a name="cfn-quicksight-analysis-barchartsortconfiguration-colorsort"></a>
The sort configuration of color fields in a bar chart\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-analysis-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesLimitConfiguration`  <a name="cfn-quicksight-analysis-barchartsortconfiguration-smallmultipleslimitconfiguration"></a>
The limit on the number of small multiples panels that are displayed\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-analysis-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiplesSort`  <a name="cfn-quicksight-analysis-barchartsortconfiguration-smallmultiplessort"></a>
The sort configuration of the small multiples field\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-analysis-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)