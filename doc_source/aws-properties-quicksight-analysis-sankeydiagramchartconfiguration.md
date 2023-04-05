# AWS::QuickSight::Analysis SankeyDiagramChartConfiguration<a name="aws-properties-quicksight-analysis-sankeydiagramchartconfiguration"></a>

The configuration of a sankey diagram\.

## Syntax<a name="aws-properties-quicksight-analysis-sankeydiagramchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sankeydiagramchartconfiguration-syntax.json"></a>

```
{
  "[DataLabels](#cfn-quicksight-analysis-sankeydiagramchartconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-analysis-sankeydiagramchartconfiguration-fieldwells)" : SankeyDiagramFieldWells,
  "[SortConfiguration](#cfn-quicksight-analysis-sankeydiagramchartconfiguration-sortconfiguration)" : SankeyDiagramSortConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-sankeydiagramchartconfiguration-syntax.yaml"></a>

```
  [DataLabels](#cfn-quicksight-analysis-sankeydiagramchartconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-analysis-sankeydiagramchartconfiguration-fieldwells): 
    SankeyDiagramFieldWells
  [SortConfiguration](#cfn-quicksight-analysis-sankeydiagramchartconfiguration-sortconfiguration): 
    SankeyDiagramSortConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-sankeydiagramchartconfiguration-properties"></a>

`DataLabels`  <a name="cfn-quicksight-analysis-sankeydiagramchartconfiguration-datalabels"></a>
The data label configuration of a sankey diagram\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-analysis-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-analysis-sankeydiagramchartconfiguration-fieldwells"></a>
The field well configuration of a sankey diagram\.  
*Required*: No  
*Type*: [SankeyDiagramFieldWells](aws-properties-quicksight-analysis-sankeydiagramfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-analysis-sankeydiagramchartconfiguration-sortconfiguration"></a>
The sort configuration of a sankey diagram\.  
*Required*: No  
*Type*: [SankeyDiagramSortConfiguration](aws-properties-quicksight-analysis-sankeydiagramsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)