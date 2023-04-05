# AWS::QuickSight::Dashboard ScatterPlotFieldWells<a name="aws-properties-quicksight-dashboard-scatterplotfieldwells"></a>

The field well configuration of a scatter plot\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-scatterplotfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-scatterplotfieldwells-syntax.json"></a>

```
{
  "[ScatterPlotCategoricallyAggregatedFieldWells](#cfn-quicksight-dashboard-scatterplotfieldwells-scatterplotcategoricallyaggregatedfieldwells)" : ScatterPlotCategoricallyAggregatedFieldWells,
  "[ScatterPlotUnaggregatedFieldWells](#cfn-quicksight-dashboard-scatterplotfieldwells-scatterplotunaggregatedfieldwells)" : ScatterPlotUnaggregatedFieldWells
}
```

### YAML<a name="aws-properties-quicksight-dashboard-scatterplotfieldwells-syntax.yaml"></a>

```
  [ScatterPlotCategoricallyAggregatedFieldWells](#cfn-quicksight-dashboard-scatterplotfieldwells-scatterplotcategoricallyaggregatedfieldwells): 
    ScatterPlotCategoricallyAggregatedFieldWells
  [ScatterPlotUnaggregatedFieldWells](#cfn-quicksight-dashboard-scatterplotfieldwells-scatterplotunaggregatedfieldwells): 
    ScatterPlotUnaggregatedFieldWells
```

## Properties<a name="aws-properties-quicksight-dashboard-scatterplotfieldwells-properties"></a>

`ScatterPlotCategoricallyAggregatedFieldWells`  <a name="cfn-quicksight-dashboard-scatterplotfieldwells-scatterplotcategoricallyaggregatedfieldwells"></a>
The aggregated field wells of a scatter plot\. Scatter plots that have a field in the category \(group/color\) field will have aggregated field wells\. The x and y\-axes of these scatter plots are aggregated by category\.  
*Required*: No  
*Type*: [ScatterPlotCategoricallyAggregatedFieldWells](aws-properties-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScatterPlotUnaggregatedFieldWells`  <a name="cfn-quicksight-dashboard-scatterplotfieldwells-scatterplotunaggregatedfieldwells"></a>
The unaggregated field wells of a scatter plot\. Scatter plots without a category field well have unaggregated field wells\. The x and y\-axes of these scatter plots are unaggregated\.  
*Required*: No  
*Type*: [ScatterPlotUnaggregatedFieldWells](aws-properties-quicksight-dashboard-scatterplotunaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)