# AWS::QuickSight::Template ComboChartAggregatedFieldWells<a name="aws-properties-quicksight-template-combochartaggregatedfieldwells"></a>

The aggregated field wells of a combo chart\.

## Syntax<a name="aws-properties-quicksight-template-combochartaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-combochartaggregatedfieldwells-syntax.json"></a>

```
{
  "[BarValues](#cfn-quicksight-template-combochartaggregatedfieldwells-barvalues)" : [ MeasureField, ... ],
  "[Category](#cfn-quicksight-template-combochartaggregatedfieldwells-category)" : [ DimensionField, ... ],
  "[Colors](#cfn-quicksight-template-combochartaggregatedfieldwells-colors)" : [ DimensionField, ... ],
  "[LineValues](#cfn-quicksight-template-combochartaggregatedfieldwells-linevalues)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-combochartaggregatedfieldwells-syntax.yaml"></a>

```
  [BarValues](#cfn-quicksight-template-combochartaggregatedfieldwells-barvalues): 
    - MeasureField
  [Category](#cfn-quicksight-template-combochartaggregatedfieldwells-category): 
    - DimensionField
  [Colors](#cfn-quicksight-template-combochartaggregatedfieldwells-colors): 
    - DimensionField
  [LineValues](#cfn-quicksight-template-combochartaggregatedfieldwells-linevalues): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-combochartaggregatedfieldwells-properties"></a>

`BarValues`  <a name="cfn-quicksight-template-combochartaggregatedfieldwells-barvalues"></a>
The aggregated `BarValues` field well of a combo chart\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Category`  <a name="cfn-quicksight-template-combochartaggregatedfieldwells-category"></a>
The aggregated category field wells of a combo chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Colors`  <a name="cfn-quicksight-template-combochartaggregatedfieldwells-colors"></a>
The aggregated colors field well of a combo chart\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LineValues`  <a name="cfn-quicksight-template-combochartaggregatedfieldwells-linevalues"></a>
The aggregated `LineValues` field well of a combo chart\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)