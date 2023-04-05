# AWS::QuickSight::Analysis TableAggregatedFieldWells<a name="aws-properties-quicksight-analysis-tableaggregatedfieldwells"></a>

The aggregated field well for the table\.

## Syntax<a name="aws-properties-quicksight-analysis-tableaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-tableaggregatedfieldwells-syntax.json"></a>

```
{
  "[GroupBy](#cfn-quicksight-analysis-tableaggregatedfieldwells-groupby)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-analysis-tableaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-tableaggregatedfieldwells-syntax.yaml"></a>

```
  [GroupBy](#cfn-quicksight-analysis-tableaggregatedfieldwells-groupby): 
    - DimensionField
  [Values](#cfn-quicksight-analysis-tableaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-tableaggregatedfieldwells-properties"></a>

`GroupBy`  <a name="cfn-quicksight-analysis-tableaggregatedfieldwells-groupby"></a>
The group by field well for a pivot table\. Values are grouped by group by fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-analysis-tableaggregatedfieldwells-values"></a>
The values field well for a pivot table\. Values are aggregated based on group by fields\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)