# AWS::QuickSight::Analysis NumericalAggregationFunction<a name="aws-properties-quicksight-analysis-numericalaggregationfunction"></a>

Aggregation for numerical values\.

## Syntax<a name="aws-properties-quicksight-analysis-numericalaggregationfunction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-numericalaggregationfunction-syntax.json"></a>

```
{
  "[PercentileAggregation](#cfn-quicksight-analysis-numericalaggregationfunction-percentileaggregation)" : PercentileAggregation,
  "[SimpleNumericalAggregation](#cfn-quicksight-analysis-numericalaggregationfunction-simplenumericalaggregation)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-numericalaggregationfunction-syntax.yaml"></a>

```
  [PercentileAggregation](#cfn-quicksight-analysis-numericalaggregationfunction-percentileaggregation): 
    PercentileAggregation
  [SimpleNumericalAggregation](#cfn-quicksight-analysis-numericalaggregationfunction-simplenumericalaggregation): String
```

## Properties<a name="aws-properties-quicksight-analysis-numericalaggregationfunction-properties"></a>

`PercentileAggregation`  <a name="cfn-quicksight-analysis-numericalaggregationfunction-percentileaggregation"></a>
An aggregation based on the percentile of values in a dimension or measure\.  
*Required*: No  
*Type*: [PercentileAggregation](aws-properties-quicksight-analysis-percentileaggregation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SimpleNumericalAggregation`  <a name="cfn-quicksight-analysis-numericalaggregationfunction-simplenumericalaggregation"></a>
Built\-in aggregation functions for numerical values\.  
+  `SUM`: The sum of a dimension or measure\. 
+  `AVERAGE`: The average of a dimension or measure\.
+  `MIN`: The minimum value of a dimension or measure\.
+  `MAX`: The maximum value of a dimension or measure\.
+  `COUNT`: The count of a dimension or measure\.
+  `DISTINCT_COUNT`: The count of distinct values in a dimension or measure\.
+  `VAR`: The variance of a dimension or measure\.
+  `VARP`: The partitioned variance of a dimension or measure\.
+  `STDEV`: The standard deviation of a dimension or measure\.
+  `STDEVP`: The partitioned standard deviation of a dimension or measure\.
+  `MEDIAN`: The median value of a dimension or measure\.
*Required*: No  
*Type*: String  
*Allowed values*: `AVERAGE | COUNT | DISTINCT_COUNT | MAX | MEDIAN | MIN | STDEV | STDEVP | SUM | VAR | VARP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)