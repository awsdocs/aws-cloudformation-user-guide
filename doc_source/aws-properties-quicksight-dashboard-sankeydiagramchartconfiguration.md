# AWS::QuickSight::Dashboard SankeyDiagramChartConfiguration<a name="aws-properties-quicksight-dashboard-sankeydiagramchartconfiguration"></a>

The configuration of a sankey diagram\.

## Syntax<a name="aws-properties-quicksight-dashboard-sankeydiagramchartconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-sankeydiagramchartconfiguration-syntax.json"></a>

```
{
  "[DataLabels](#cfn-quicksight-dashboard-sankeydiagramchartconfiguration-datalabels)" : DataLabelOptions,
  "[FieldWells](#cfn-quicksight-dashboard-sankeydiagramchartconfiguration-fieldwells)" : SankeyDiagramFieldWells,
  "[SortConfiguration](#cfn-quicksight-dashboard-sankeydiagramchartconfiguration-sortconfiguration)" : SankeyDiagramSortConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-sankeydiagramchartconfiguration-syntax.yaml"></a>

```
  [DataLabels](#cfn-quicksight-dashboard-sankeydiagramchartconfiguration-datalabels): 
    DataLabelOptions
  [FieldWells](#cfn-quicksight-dashboard-sankeydiagramchartconfiguration-fieldwells): 
    SankeyDiagramFieldWells
  [SortConfiguration](#cfn-quicksight-dashboard-sankeydiagramchartconfiguration-sortconfiguration): 
    SankeyDiagramSortConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-sankeydiagramchartconfiguration-properties"></a>

`DataLabels`  <a name="cfn-quicksight-dashboard-sankeydiagramchartconfiguration-datalabels"></a>
The data label configuration of a sankey diagram\.  
*Required*: No  
*Type*: [DataLabelOptions](aws-properties-quicksight-dashboard-datalabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldWells`  <a name="cfn-quicksight-dashboard-sankeydiagramchartconfiguration-fieldwells"></a>
The field well configuration of a sankey diagram\.  
*Required*: No  
*Type*: [SankeyDiagramFieldWells](aws-properties-quicksight-dashboard-sankeydiagramfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SortConfiguration`  <a name="cfn-quicksight-dashboard-sankeydiagramchartconfiguration-sortconfiguration"></a>
The sort configuration of a sankey diagram\.  
*Required*: No  
*Type*: [SankeyDiagramSortConfiguration](aws-properties-quicksight-dashboard-sankeydiagramsortconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)