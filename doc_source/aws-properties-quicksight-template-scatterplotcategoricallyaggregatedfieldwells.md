# AWS::QuickSight::Template ScatterPlotCategoricallyAggregatedFieldWells<a name="aws-properties-quicksight-template-scatterplotcategoricallyaggregatedfieldwells"></a>

The aggregated field well of a scatter plot\.

## Syntax<a name="aws-properties-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Size](#cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-size)" : [ MeasureField, ... ],
  "[XAxis](#cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-xaxis)" : [ MeasureField, ... ],
  "[YAxis](#cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-yaxis)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-category): 
    - DimensionField
  [Size](#cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-size): 
    - MeasureField
  [XAxis](#cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-xaxis): 
    - MeasureField
  [YAxis](#cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-yaxis): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-category"></a>
The category field well of a scatter plot\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-size"></a>
The size field well of a scatter plot\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxis`  <a name="cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-xaxis"></a>
The x\-axis field well of a scatter plot\.  
The x\-axis is aggregated by category\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxis`  <a name="cfn-quicksight-template-scatterplotcategoricallyaggregatedfieldwells-yaxis"></a>
The y\-axis field well of a scatter plot\.  
The y\-axis is aggregated by category\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)