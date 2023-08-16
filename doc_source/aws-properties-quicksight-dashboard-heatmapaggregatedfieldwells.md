# AWS::QuickSight::Dashboard HeatMapAggregatedFieldWells<a name="aws-properties-quicksight-dashboard-heatmapaggregatedfieldwells"></a>

The aggregated field wells of a heat map\.

## Syntax<a name="aws-properties-quicksight-dashboard-heatmapaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-heatmapaggregatedfieldwells-syntax.json"></a>

```
{
  "[Columns](#cfn-quicksight-dashboard-heatmapaggregatedfieldwells-columns)" : [ DimensionField, ... ],
  "[Rows](#cfn-quicksight-dashboard-heatmapaggregatedfieldwells-rows)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-dashboard-heatmapaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-heatmapaggregatedfieldwells-syntax.yaml"></a>

```
  [Columns](#cfn-quicksight-dashboard-heatmapaggregatedfieldwells-columns): 
    - DimensionField
  [Rows](#cfn-quicksight-dashboard-heatmapaggregatedfieldwells-rows): 
    - DimensionField
  [Values](#cfn-quicksight-dashboard-heatmapaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-heatmapaggregatedfieldwells-properties"></a>

`Columns`  <a name="cfn-quicksight-dashboard-heatmapaggregatedfieldwells-columns"></a>
The columns field well of a heat map\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rows`  <a name="cfn-quicksight-dashboard-heatmapaggregatedfieldwells-rows"></a>
The rows field well of a heat map\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-dashboard-heatmapaggregatedfieldwells-values"></a>
The values field well of a heat map\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)