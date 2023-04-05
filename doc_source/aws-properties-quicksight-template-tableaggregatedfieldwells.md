# AWS::QuickSight::Template TableAggregatedFieldWells<a name="aws-properties-quicksight-template-tableaggregatedfieldwells"></a>

The aggregated field well for the table\.

## Syntax<a name="aws-properties-quicksight-template-tableaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-tableaggregatedfieldwells-syntax.json"></a>

```
{
  "[GroupBy](#cfn-quicksight-template-tableaggregatedfieldwells-groupby)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-template-tableaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-tableaggregatedfieldwells-syntax.yaml"></a>

```
  [GroupBy](#cfn-quicksight-template-tableaggregatedfieldwells-groupby): 
    - DimensionField
  [Values](#cfn-quicksight-template-tableaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-tableaggregatedfieldwells-properties"></a>

`GroupBy`  <a name="cfn-quicksight-template-tableaggregatedfieldwells-groupby"></a>
The group by field well for a pivot table\. Values are grouped by group by fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-template-tableaggregatedfieldwells-values"></a>
The values field well for a pivot table\. Values are aggregated based on group by fields\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)