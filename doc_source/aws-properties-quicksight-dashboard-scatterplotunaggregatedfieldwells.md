# AWS::QuickSight::Dashboard ScatterPlotUnaggregatedFieldWells<a name="aws-properties-quicksight-dashboard-scatterplotunaggregatedfieldwells"></a>

The unaggregated field wells of a scatter plot\.

## Syntax<a name="aws-properties-quicksight-dashboard-scatterplotunaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-scatterplotunaggregatedfieldwells-syntax.json"></a>

```
{
  "[Size](#cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-size)" : [ MeasureField, ... ],
  "[XAxis](#cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-xaxis)" : [ DimensionField, ... ],
  "[YAxis](#cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-yaxis)" : [ DimensionField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-scatterplotunaggregatedfieldwells-syntax.yaml"></a>

```
  [Size](#cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-size): 
    - MeasureField
  [XAxis](#cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-xaxis): 
    - DimensionField
  [YAxis](#cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-yaxis): 
    - DimensionField
```

## Properties<a name="aws-properties-quicksight-dashboard-scatterplotunaggregatedfieldwells-properties"></a>

`Size`  <a name="cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-size"></a>
The size field well of a scatter plot\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxis`  <a name="cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-xaxis"></a>
The x\-axis field well of a scatter plot\.  
The x\-axis is a dimension field and cannot be aggregated\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxis`  <a name="cfn-quicksight-dashboard-scatterplotunaggregatedfieldwells-yaxis"></a>
The y\-axis field well of a scatter plot\.  
The y\-axis is a dimension field and cannot be aggregated\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)