# AWS::QuickSight::Template PieChartAggregatedFieldWells<a name="aws-properties-quicksight-template-piechartaggregatedfieldwells"></a>

The field well configuration of a pie chart\.

## Syntax<a name="aws-properties-quicksight-template-piechartaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-piechartaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-template-piechartaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[SmallMultiples](#cfn-quicksight-template-piechartaggregatedfieldwells-smallmultiples)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-template-piechartaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-piechartaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-template-piechartaggregatedfieldwells-category): 
    - DimensionField
  [SmallMultiples](#cfn-quicksight-template-piechartaggregatedfieldwells-smallmultiples): 
    - DimensionField
  [Values](#cfn-quicksight-template-piechartaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-piechartaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-template-piechartaggregatedfieldwells-category"></a>
The category \(group/color\) field wells of a pie chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiples`  <a name="cfn-quicksight-template-piechartaggregatedfieldwells-smallmultiples"></a>
The small multiples field well of a pie chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-template-piechartaggregatedfieldwells-values"></a>
The value field wells of a pie chart\. Values are aggregated based on categories\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)