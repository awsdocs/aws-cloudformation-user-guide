# AWS::QuickSight::Analysis BarChartAggregatedFieldWells<a name="aws-properties-quicksight-analysis-barchartaggregatedfieldwells"></a>

The aggregated field wells of a bar chart\.

## Syntax<a name="aws-properties-quicksight-analysis-barchartaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-barchartaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-analysis-barchartaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Colors](#cfn-quicksight-analysis-barchartaggregatedfieldwells-colors)" : [ DimensionField, ... ],
  "[SmallMultiples](#cfn-quicksight-analysis-barchartaggregatedfieldwells-smallmultiples)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-analysis-barchartaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-barchartaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-analysis-barchartaggregatedfieldwells-category): 
    - DimensionField
  [Colors](#cfn-quicksight-analysis-barchartaggregatedfieldwells-colors): 
    - DimensionField
  [SmallMultiples](#cfn-quicksight-analysis-barchartaggregatedfieldwells-smallmultiples): 
    - DimensionField
  [Values](#cfn-quicksight-analysis-barchartaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-barchartaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-analysis-barchartaggregatedfieldwells-category"></a>
The category \(y\-axis\) field well of a bar chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Colors`  <a name="cfn-quicksight-analysis-barchartaggregatedfieldwells-colors"></a>
The color \(group/color\) field well of a bar chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmallMultiples`  <a name="cfn-quicksight-analysis-barchartaggregatedfieldwells-smallmultiples"></a>
The small multiples field well of a bar chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-analysis-barchartaggregatedfieldwells-values"></a>
The value field wells of a bar chart\. Values are aggregated by category\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)