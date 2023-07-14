# AWS::QuickSight::Dashboard ReferenceLineDynamicDataConfiguration<a name="aws-properties-quicksight-dashboard-referencelinedynamicdataconfiguration"></a>

The dynamic configuration of the reference line data configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-referencelinedynamicdataconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-referencelinedynamicdataconfiguration-syntax.json"></a>

```
{
  "[Calculation](#cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-calculation)" : NumericalAggregationFunction,
  "[Column](#cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-column)" : ColumnIdentifier,
  "[MeasureAggregationFunction](#cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-measureaggregationfunction)" : AggregationFunction
}
```

### YAML<a name="aws-properties-quicksight-dashboard-referencelinedynamicdataconfiguration-syntax.yaml"></a>

```
  [Calculation](#cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-calculation): 
    NumericalAggregationFunction
  [Column](#cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-column): 
    ColumnIdentifier
  [MeasureAggregationFunction](#cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-measureaggregationfunction): 
    AggregationFunction
```

## Properties<a name="aws-properties-quicksight-dashboard-referencelinedynamicdataconfiguration-properties"></a>

`Calculation`  <a name="cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-calculation"></a>
The calculation that is used in the dynamic data\.  
*Required*: Yes  
*Type*: [NumericalAggregationFunction](aws-properties-quicksight-dashboard-numericalaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-column"></a>
The column that the dynamic data targets\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MeasureAggregationFunction`  <a name="cfn-quicksight-dashboard-referencelinedynamicdataconfiguration-measureaggregationfunction"></a>
The aggregation function that is used in the dynamic data\.  
*Required*: No  
*Type*: [AggregationFunction](aws-properties-quicksight-dashboard-aggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)