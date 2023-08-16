# AWS::QuickSight::Dashboard ScatterPlotCategoricallyAggregatedFieldWells<a name="aws-properties-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells"></a>

The aggregated field well of a scatter plot\.

## Syntax<a name="aws-properties-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Label](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-label)" : [ DimensionField, ... ],
  "[Size](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-size)" : [ MeasureField, ... ],
  "[XAxis](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-xaxis)" : [ MeasureField, ... ],
  "[YAxis](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-yaxis)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-category): 
    - DimensionField
  [Label](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-label): 
    - DimensionField
  [Size](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-size): 
    - MeasureField
  [XAxis](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-xaxis): 
    - MeasureField
  [YAxis](#cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-yaxis): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-category"></a>
The category field well of a scatter plot\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Label`  <a name="cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-label"></a>
The label field well of a scatter plot\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-size"></a>
The size field well of a scatter plot\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxis`  <a name="cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-xaxis"></a>
The x\-axis field well of a scatter plot\.  
The x\-axis is aggregated by category\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxis`  <a name="cfn-quicksight-dashboard-scatterplotcategoricallyaggregatedfieldwells-yaxis"></a>
The y\-axis field well of a scatter plot\.  
The y\-axis is aggregated by category\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)