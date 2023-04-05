# AWS::QuickSight::Dashboard WordCloudAggregatedFieldWells<a name="aws-properties-quicksight-dashboard-wordcloudaggregatedfieldwells"></a>

The aggregated field wells of a word cloud\.

## Syntax<a name="aws-properties-quicksight-dashboard-wordcloudaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-wordcloudaggregatedfieldwells-syntax.json"></a>

```
{
  "[GroupBy](#cfn-quicksight-dashboard-wordcloudaggregatedfieldwells-groupby)" : [ DimensionField, ... ],
  "[Size](#cfn-quicksight-dashboard-wordcloudaggregatedfieldwells-size)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-wordcloudaggregatedfieldwells-syntax.yaml"></a>

```
  [GroupBy](#cfn-quicksight-dashboard-wordcloudaggregatedfieldwells-groupby): 
    - DimensionField
  [Size](#cfn-quicksight-dashboard-wordcloudaggregatedfieldwells-size): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-wordcloudaggregatedfieldwells-properties"></a>

`GroupBy`  <a name="cfn-quicksight-dashboard-wordcloudaggregatedfieldwells-groupby"></a>
The group by field well of a word cloud\. Values are grouped by group by fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-quicksight-dashboard-wordcloudaggregatedfieldwells-size"></a>
The size field well of a word cloud\. Values are aggregated based on group by fields\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)