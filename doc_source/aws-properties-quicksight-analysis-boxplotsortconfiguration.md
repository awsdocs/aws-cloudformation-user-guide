# AWS::QuickSight::Analysis BoxPlotSortConfiguration<a name="aws-properties-quicksight-analysis-boxplotsortconfiguration"></a>

The sort configuration of a `BoxPlotVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-boxplotsortconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-boxplotsortconfiguration-syntax.json"></a>

```
{
  "[CategorySort](#cfn-quicksight-analysis-boxplotsortconfiguration-categorysort)" : [ FieldSortOptions, ... ],
  "[PaginationConfiguration](#cfn-quicksight-analysis-boxplotsortconfiguration-paginationconfiguration)" : PaginationConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-boxplotsortconfiguration-syntax.yaml"></a>

```
  [CategorySort](#cfn-quicksight-analysis-boxplotsortconfiguration-categorysort): 
    - FieldSortOptions
  [PaginationConfiguration](#cfn-quicksight-analysis-boxplotsortconfiguration-paginationconfiguration): 
    PaginationConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-boxplotsortconfiguration-properties"></a>

`CategorySort`  <a name="cfn-quicksight-analysis-boxplotsortconfiguration-categorysort"></a>
The sort configuration of a group by fields\.  
*Required*: No  
*Type*: List of [FieldSortOptions](aws-properties-quicksight-analysis-fieldsortoptions.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaginationConfiguration`  <a name="cfn-quicksight-analysis-boxplotsortconfiguration-paginationconfiguration"></a>
The pagination configuration of a table visual or box plot\.  
*Required*: No  
*Type*: [PaginationConfiguration](aws-properties-quicksight-analysis-paginationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)