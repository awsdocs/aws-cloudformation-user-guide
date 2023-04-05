# AWS::QuickSight::Template ScatterPlotFieldWells<a name="aws-properties-quicksight-template-scatterplotfieldwells"></a>

The field well configuration of a scatter plot\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-scatterplotfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-scatterplotfieldwells-syntax.json"></a>

```
{
  "[ScatterPlotCategoricallyAggregatedFieldWells](#cfn-quicksight-template-scatterplotfieldwells-scatterplotcategoricallyaggregatedfieldwells)" : ScatterPlotCategoricallyAggregatedFieldWells,
  "[ScatterPlotUnaggregatedFieldWells](#cfn-quicksight-template-scatterplotfieldwells-scatterplotunaggregatedfieldwells)" : ScatterPlotUnaggregatedFieldWells
}
```

### YAML<a name="aws-properties-quicksight-template-scatterplotfieldwells-syntax.yaml"></a>

```
  [ScatterPlotCategoricallyAggregatedFieldWells](#cfn-quicksight-template-scatterplotfieldwells-scatterplotcategoricallyaggregatedfieldwells): 
    ScatterPlotCategoricallyAggregatedFieldWells
  [ScatterPlotUnaggregatedFieldWells](#cfn-quicksight-template-scatterplotfieldwells-scatterplotunaggregatedfieldwells): 
    ScatterPlotUnaggregatedFieldWells
```

## Properties<a name="aws-properties-quicksight-template-scatterplotfieldwells-properties"></a>

`ScatterPlotCategoricallyAggregatedFieldWells`  <a name="cfn-quicksight-template-scatterplotfieldwells-scatterplotcategoricallyaggregatedfieldwells"></a>
The aggregated field wells of a scatter plot\. Scatter plots that have a field in the category \(group/color\) field will have aggregated field wells\. The x and y\-axes of these scatter plots are aggregated by category\.  
*Required*: No  
*Type*: [ScatterPlotCategoricallyAggregatedFieldWells](aws-properties-quicksight-template-scatterplotcategoricallyaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScatterPlotUnaggregatedFieldWells`  <a name="cfn-quicksight-template-scatterplotfieldwells-scatterplotunaggregatedfieldwells"></a>
The unaggregated field wells of a scatter plot\. Scatter plots without a category field well have unaggregated field wells\. The x and y\-axes of these scatter plots are unaggregated\.  
*Required*: No  
*Type*: [ScatterPlotUnaggregatedFieldWells](aws-properties-quicksight-template-scatterplotunaggregatedfieldwells.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)