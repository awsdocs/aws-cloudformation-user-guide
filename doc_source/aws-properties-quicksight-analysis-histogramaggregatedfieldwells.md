# AWS::QuickSight::Analysis HistogramAggregatedFieldWells<a name="aws-properties-quicksight-analysis-histogramaggregatedfieldwells"></a>

The field well configuration of a histogram\.

## Syntax<a name="aws-properties-quicksight-analysis-histogramaggregatedfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-histogramaggregatedfieldwells-syntax.json"></a>

```
{
  "[Values](#cfn-quicksight-analysis-histogramaggregatedfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-histogramaggregatedfieldwells-syntax.yaml"></a>

```
  [Values](#cfn-quicksight-analysis-histogramaggregatedfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-histogramaggregatedfieldwells-properties"></a>

`Values`  <a name="cfn-quicksight-analysis-histogramaggregatedfieldwells-values"></a>
The value field wells of a histogram\. Values are aggregated by `COUNT` or `DISTINCT_COUNT`\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)