# AWS::QuickSight::Dashboard FunnelChartAggregatedFieldWells<a name="aws-properties-quicksight-dashboard-funnelchartaggregatedfieldwells"></a>

The field well configuration of a `FunnelChartVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-funnelchartaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-funnelchartaggregatedfieldwells-syntax.json"></a>

```
{
  "[Category](#cfn-quicksight-dashboard-funnelchartaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-dashboard-funnelchartaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-funnelchartaggregatedfieldwells-syntax.yaml"></a>

```
  [Category](#cfn-quicksight-dashboard-funnelchartaggregatedfieldwells-category): 
    - DimensionField
  [Values](#cfn-quicksight-dashboard-funnelchartaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-funnelchartaggregatedfieldwells-properties"></a>

`Category`  <a name="cfn-quicksight-dashboard-funnelchartaggregatedfieldwells-category"></a>
The category field wells of a funnel chart\. Values are grouped by category fields\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-dashboard-funnelchartaggregatedfieldwells-values"></a>
The value field wells of a funnel chart\. Values are aggregated based on categories\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)