# AWS::QuickSight::Template ReferenceLineDynamicDataConfiguration<a name="aws-properties-quicksight-template-referencelinedynamicdataconfiguration"></a>

The dynamic configuration of the reference line data configuration\.

## Syntax<a name="aws-properties-quicksight-template-referencelinedynamicdataconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-referencelinedynamicdataconfiguration-syntax.json"></a>

```
{
  "[Calculation](#cfn-quicksight-template-referencelinedynamicdataconfiguration-calculation)" : NumericalAggregationFunction,
  "[Column](#cfn-quicksight-template-referencelinedynamicdataconfiguration-column)" : ColumnIdentifier,
  "[MeasureAggregationFunction](#cfn-quicksight-template-referencelinedynamicdataconfiguration-measureaggregationfunction)" : AggregationFunction
}
```

### YAML<a name="aws-properties-quicksight-template-referencelinedynamicdataconfiguration-syntax.yaml"></a>

```
  [Calculation](#cfn-quicksight-template-referencelinedynamicdataconfiguration-calculation): 
    NumericalAggregationFunction
  [Column](#cfn-quicksight-template-referencelinedynamicdataconfiguration-column): 
    ColumnIdentifier
  [MeasureAggregationFunction](#cfn-quicksight-template-referencelinedynamicdataconfiguration-measureaggregationfunction): 
    AggregationFunction
```

## Properties<a name="aws-properties-quicksight-template-referencelinedynamicdataconfiguration-properties"></a>

`Calculation`  <a name="cfn-quicksight-template-referencelinedynamicdataconfiguration-calculation"></a>
The calculation that is used in the dynamic data\.  
*Required*: Yes  
*Type*: [NumericalAggregationFunction](aws-properties-quicksight-template-numericalaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-template-referencelinedynamicdataconfiguration-column"></a>
The column that the dynamic data targets\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MeasureAggregationFunction`  <a name="cfn-quicksight-template-referencelinedynamicdataconfiguration-measureaggregationfunction"></a>
The aggregation function that is used in the dynamic data\.  
*Required*: No  
*Type*: [AggregationFunction](aws-properties-quicksight-template-aggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)