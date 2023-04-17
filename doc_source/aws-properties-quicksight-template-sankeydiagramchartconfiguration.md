# AWS::QuickSight::Template SankeyDiagramChartConfiguration<a name="aws-properties-quicksight-template-sankeydiagramchartconfiguration"></a>

The configuration of a sankey diagram\.

## Syntax<a name="aws-properties-quicksight-template-sankeydiagramchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-sankeydiagramchartconfiguration-syntax.json"></a>

```
{
  "[DataLabels](#cfn-quicksight-template-sankeydiagramchartconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-template-sankeydiagramchartconfiguration-fieldwells)" : SankeyDiagramFieldWells,
  "[SortConfiguration](#cfn-quicksight-template-sankeydiagramchartconfiguration-sortconfiguration)" : SankeyDiagramSortConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-sankeydiagramchartconfiguration-syntax.yaml"></a>

```
  [DataLabels](#cfn-quicksight-template-sankeydiagramchartconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-template-sankeydiagramchartconfiguration-fieldwells): 
    SankeyDiagramFieldWells
  [SortConfiguration](#cfn-quicksight-template-sankeydiagramchartconfiguration-sortconfiguration): 
    SankeyDiagramSortConfiguration
```

## Properties<a name="aws-properties-quicksight-template-sankeydiagramchartconfiguration-properties"></a>

`DataLabels`  <a name="cfn-quicksight-template-sankeydiagramchartconfiguration-datalabels"></a>
The data label configuration of a sankey diagram\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-template-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-template-sankeydiagramchartconfiguration-fieldwells"></a>
The field well configuration of a sankey diagram\.  
*Required*: No  
*Type*: [SankeyDiagramFieldWells](aws-properties-quicksight-template-sankeydiagramfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-template-sankeydiagramchartconfiguration-sortconfiguration"></a>
The sort configuration of a sankey diagram\.  
*Required*: No  
*Type*: [SankeyDiagramSortConfiguration](aws-properties-quicksight-template-sankeydiagramsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)