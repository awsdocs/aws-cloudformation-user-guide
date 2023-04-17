# AWS::QuickSight::Template FunnelChartAggregatedFieldWells<a name="aws-properties-quicksight-template-funnelchartaggregatedfieldwells"></a>

The field well configuration of a `FunnelChartVisual`\.

## Syntax<a name="aws-properties-quicksight-template-funnelchartaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-funnelchartaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-template-funnelchartaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-template-funnelchartaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-funnelchartaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-template-funnelchartaggregatedfieldwells-category): 
    - DimensionField
  [Values](#cfn-quicksight-template-funnelchartaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-funnelchartaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-template-funnelchartaggregatedfieldwells-category"></a>
The category field wells of a funnel chart\. Values are grouped by category fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-template-funnelchartaggregatedfieldwells-values"></a>
The value field wells of a funnel chart\. Values are aggregated based on categories\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)