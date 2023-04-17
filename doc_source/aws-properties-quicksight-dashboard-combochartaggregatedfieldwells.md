# AWS::QuickSight::Dashboard ComboChartAggregatedFieldWells<a name="aws-properties-quicksight-dashboard-combochartaggregatedfieldwells"></a>

The aggregated field wells of a combo chart\.

## Syntax<a name="aws-properties-quicksight-dashboard-combochartaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-combochartaggregatedfieldwells-syntax.json"></a>

```
{
  "[BarValues](#cfn-quicksight-dashboard-combochartaggregatedfieldwells-barvalues)" : [ MeasureField, ... ],
  "[Category](#cfn-quicksight-dashboard-combochartaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Colors](#cfn-quicksight-dashboard-combochartaggregatedfieldwells-colors)" : [ DimensionField, ... ],
  "[LineValues](#cfn-quicksight-dashboard-combochartaggregatedfieldwells-linevalues)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-combochartaggregatedfieldwells-syntax.yaml"></a>

```
  [BarValues](#cfn-quicksight-dashboard-combochartaggregatedfieldwells-barvalues): 
    - MeasureField
  [Category](#cfn-quicksight-dashboard-combochartaggregatedfieldwells-category): 
    - DimensionField
  [Colors](#cfn-quicksight-dashboard-combochartaggregatedfieldwells-colors): 
    - DimensionField
  [LineValues](#cfn-quicksight-dashboard-combochartaggregatedfieldwells-linevalues): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-dashboard-combochartaggregatedfieldwells-properties"></a>

`BarValues`  <a name="cfn-quicksight-dashboard-combochartaggregatedfieldwells-barvalues"></a>
The aggregated `BarValues` field well of a combo chart\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Category`  <a name="cfn-quicksight-dashboard-combochartaggregatedfieldwells-category"></a>
The aggregated category field wells of a combo chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Colors`  <a name="cfn-quicksight-dashboard-combochartaggregatedfieldwells-colors"></a>
The aggregated colors field well of a combo chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-dashboard-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineValues`  <a name="cfn-quicksight-dashboard-combochartaggregatedfieldwells-linevalues"></a>
The aggregated `LineValues` field well of a combo chart\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-dashboard-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)