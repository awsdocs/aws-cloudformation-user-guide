# AWS::QuickSight::Template BoxPlotAggregatedFieldWells<a name="aws-properties-quicksight-template-boxplotaggregatedfieldwells"></a>

The aggregated field well for a box plot\.

## Syntax<a name="aws-properties-quicksight-template-boxplotaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-boxplotaggregatedfieldwells-syntax.json"></a>

```
{
  "[GroupBy](#cfn-quicksight-template-boxplotaggregatedfieldwells-groupby)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-template-boxplotaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-boxplotaggregatedfieldwells-syntax.yaml"></a>

```
  [GroupBy](#cfn-quicksight-template-boxplotaggregatedfieldwells-groupby): 
    - DimensionField
  [Values](#cfn-quicksight-template-boxplotaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-boxplotaggregatedfieldwells-properties"></a>

`GroupBy`  <a name="cfn-quicksight-template-boxplotaggregatedfieldwells-groupby"></a>
The group by field well of a box plot chart\. Values are grouped based on group by fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-template-boxplotaggregatedfieldwells-values"></a>
The value field well of a box plot chart\. Values are aggregated based on group by fields\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)