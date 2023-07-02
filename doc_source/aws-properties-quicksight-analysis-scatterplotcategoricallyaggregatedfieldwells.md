# AWS::QuickSight::Analysis ScatterPlotCategoricallyAggregatedFieldWells<a name="aws-properties-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells"></a>

The aggregated field well of a scatter plot\.

## Syntax<a name="aws-properties-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Label](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-label)" : [ DimensionField, ... ],
  "[Size](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-size)" : [ MeasureField, ... ],
  "[XAxis](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-xaxis)" : [ MeasureField, ... ],
  "[YAxis](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-yaxis)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-category): 
    - DimensionField
  [Label](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-label): 
    - DimensionField
  [Size](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-size): 
    - MeasureField
  [XAxis](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-xaxis): 
    - MeasureField
  [YAxis](#cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-yaxis): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-category"></a>
The category field well of a scatter plot\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Label`  <a name="cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-label"></a>
The label field well of a scatter plot\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-size"></a>
The size field well of a scatter plot\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxis`  <a name="cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-xaxis"></a>
The x\-axis field well of a scatter plot\.  
The x\-axis is aggregated by category\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxis`  <a name="cfn-quicksight-analysis-scatterplotcategoricallyaggregatedfieldwells-yaxis"></a>
The y\-axis field well of a scatter plot\.  
The y\-axis is aggregated by category\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)