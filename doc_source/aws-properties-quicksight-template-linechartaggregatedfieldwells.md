# AWS::QuickSight::Template LineChartAggregatedFieldWells<a name="aws-properties-quicksight-template-linechartaggregatedfieldwells"></a>

The field well configuration of a line chart\.

## Syntax<a name="aws-properties-quicksight-template-linechartaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-linechartaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-template-linechartaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Colors](#cfn-quicksight-template-linechartaggregatedfieldwells-colors)" : [ DimensionField, ... ],
  "[SmallMultiples](#cfn-quicksight-template-linechartaggregatedfieldwells-smallmultiples)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-template-linechartaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-linechartaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-template-linechartaggregatedfieldwells-category): 
    - DimensionField
  [Colors](#cfn-quicksight-template-linechartaggregatedfieldwells-colors): 
    - DimensionField
  [SmallMultiples](#cfn-quicksight-template-linechartaggregatedfieldwells-smallmultiples): 
    - DimensionField
  [Values](#cfn-quicksight-template-linechartaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-linechartaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-template-linechartaggregatedfieldwells-category"></a>
The category field wells of a line chart\. Values are grouped by category fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Colors`  <a name="cfn-quicksight-template-linechartaggregatedfieldwells-colors"></a>
The color field wells of a line chart\. Values are grouped by category fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiples`  <a name="cfn-quicksight-template-linechartaggregatedfieldwells-smallmultiples"></a>
The small multiples field well of a line chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-template-linechartaggregatedfieldwells-values"></a>
The value field wells of a line chart\. Values are aggregated based on categories\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)