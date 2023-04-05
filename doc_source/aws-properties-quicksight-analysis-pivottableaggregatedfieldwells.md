# AWS::QuickSight::Analysis PivotTableAggregatedFieldWells<a name="aws-properties-quicksight-analysis-pivottableaggregatedfieldwells"></a>

The aggregated field well for the pivot table\.

## Syntax<a name="aws-properties-quicksight-analysis-pivottableaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-pivottableaggregatedfieldwells-syntax.json"></a>

```
{
  "[Columns](#cfn-quicksight-analysis-pivottableaggregatedfieldwells-columns)" : [ DimensionField, ... ],
  "[Rows](#cfn-quicksight-analysis-pivottableaggregatedfieldwells-rows)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-analysis-pivottableaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-pivottableaggregatedfieldwells-syntax.yaml"></a>

```
  [Columns](#cfn-quicksight-analysis-pivottableaggregatedfieldwells-columns): 
    - DimensionField
  [Rows](#cfn-quicksight-analysis-pivottableaggregatedfieldwells-rows): 
    - DimensionField
  [Values](#cfn-quicksight-analysis-pivottableaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-pivottableaggregatedfieldwells-properties"></a>

`Columns`  <a name="cfn-quicksight-analysis-pivottableaggregatedfieldwells-columns"></a>
The columns field well for a pivot table\. Values are grouped by columns fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `40`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rows`  <a name="cfn-quicksight-analysis-pivottableaggregatedfieldwells-rows"></a>
The rows field well for a pivot table\. Values are grouped by rows fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `40`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-analysis-pivottableaggregatedfieldwells-values"></a>
The values field well for a pivot table\. Values are aggregated based on rows and columns fields\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `40`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)