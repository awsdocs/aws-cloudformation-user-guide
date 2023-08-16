# AWS::QuickSight::Analysis SankeyDiagramSortConfiguration<a name="aws-properties-quicksight-analysis-sankeydiagramsortconfiguration"></a>

The sort configuration of a sankey diagram\.

## Syntax<a name="aws-properties-quicksight-analysis-sankeydiagramsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sankeydiagramsortconfiguration-syntax.json"></a>

```
{
  "[DestinationItemsLimit](#cfn-quicksight-analysis-sankeydiagramsortconfiguration-destinationitemslimit)" : ItemsLimitConfiguration,
  "[SourceItemsLimit](#cfn-quicksight-analysis-sankeydiagramsortconfiguration-sourceitemslimit)" : ItemsLimitConfiguration,
  "[WeightSort](#cfn-quicksight-analysis-sankeydiagramsortconfiguration-weightsort)" : [ FieldSortOptions, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-sankeydiagramsortconfiguration-syntax.yaml"></a>

```
  [DestinationItemsLimit](#cfn-quicksight-analysis-sankeydiagramsortconfiguration-destinationitemslimit): 
    ItemsLimitConfiguration
  [SourceItemsLimit](#cfn-quicksight-analysis-sankeydiagramsortconfiguration-sourceitemslimit): 
    ItemsLimitConfiguration
  [WeightSort](#cfn-quicksight-analysis-sankeydiagramsortconfiguration-weightsort): 
    - FieldSortOptions
```

## Properties<a name="aws-properties-quicksight-analysis-sankeydiagramsortconfiguration-properties"></a>

`DestinationItemsLimit`  <a name="cfn-quicksight-analysis-sankeydiagramsortconfiguration-destinationitemslimit"></a>
The limit on the number of destination nodes that are displayed in a sankey diagram\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-analysis-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceItemsLimit`  <a name="cfn-quicksight-analysis-sankeydiagramsortconfiguration-sourceitemslimit"></a>
The limit on the number of source nodes that are displayed in a sankey diagram\.  
*Required*: No  
*Type*: [ItemsLimitConfiguration](aws-properties-quicksight-analysis-itemslimitconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeightSort`  <a name="cfn-quicksight-analysis-sankeydiagramsortconfiguration-weightsort"></a>
The sort configuration of the weight fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-analysis-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)