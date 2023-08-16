# AWS::QuickSight::Analysis LineChartAggregatedFieldWells<a name="aws-properties-quicksight-analysis-linechartaggregatedfieldwells"></a>

The field well configuration of a line chart\.

## Syntax<a name="aws-properties-quicksight-analysis-linechartaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-linechartaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-analysis-linechartaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Colors](#cfn-quicksight-analysis-linechartaggregatedfieldwells-colors)" : [ DimensionField, ... ],
  "[SmallMultiples](#cfn-quicksight-analysis-linechartaggregatedfieldwells-smallmultiples)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-analysis-linechartaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-linechartaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-analysis-linechartaggregatedfieldwells-category): 
    - DimensionField
  [Colors](#cfn-quicksight-analysis-linechartaggregatedfieldwells-colors): 
    - DimensionField
  [SmallMultiples](#cfn-quicksight-analysis-linechartaggregatedfieldwells-smallmultiples): 
    - DimensionField
  [Values](#cfn-quicksight-analysis-linechartaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-linechartaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-analysis-linechartaggregatedfieldwells-category"></a>
The category field wells of a line chart\. Values are grouped by category fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Colors`  <a name="cfn-quicksight-analysis-linechartaggregatedfieldwells-colors"></a>
The color field wells of a line chart\. Values are grouped by category fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiples`  <a name="cfn-quicksight-analysis-linechartaggregatedfieldwells-smallmultiples"></a>
The small multiples field well of a line chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-analysis-linechartaggregatedfieldwells-values"></a>
The value field wells of a line chart\. Values are aggregated based on categories\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)