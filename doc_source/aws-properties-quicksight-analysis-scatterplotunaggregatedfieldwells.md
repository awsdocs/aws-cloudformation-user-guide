# AWS::QuickSight::Analysis ScatterPlotUnaggregatedFieldWells<a name="aws-properties-quicksight-analysis-scatterplotunaggregatedfieldwells"></a>

The unaggregated field wells of a scatter plot\.

## Syntax<a name="aws-properties-quicksight-analysis-scatterplotunaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-scatterplotunaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Label](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-label)" : [ DimensionField, ... ],
  "[Size](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-size)" : [ MeasureField, ... ],
  "[XAxis](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-xaxis)" : [ DimensionField, ... ],
  "[YAxis](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-yaxis)" : [ DimensionField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-scatterplotunaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-category): 
    - DimensionField
  [Label](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-label): 
    - DimensionField
  [Size](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-size): 
    - MeasureField
  [XAxis](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-xaxis): 
    - DimensionField
  [YAxis](#cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-yaxis): 
    - DimensionField
```

## Properties<a name="aws-properties-quicksight-analysis-scatterplotunaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-category"></a>
The category field well of a scatter plot\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Label`  <a name="cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-label"></a>
The label field well of a scatter plot\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-size"></a>
The size field well of a scatter plot\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxis`  <a name="cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-xaxis"></a>
The x\-axis field well of a scatter plot\.  
The x\-axis is a dimension field and cannot be aggregated\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxis`  <a name="cfn-quicksight-analysis-scatterplotunaggregatedfieldwells-yaxis"></a>
The y\-axis field well of a scatter plot\.  
The y\-axis is a dimension field and cannot be aggregated\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)