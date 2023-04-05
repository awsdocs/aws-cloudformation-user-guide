# AWS::QuickSight::Template AggregationFunction<a name="aws-properties-quicksight-template-aggregationfunction"></a>

An aggregation function aggregates values from a dimension or measure\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-aggregationfunction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-aggregationfunction-syntax.json"></a>

```
{
  "[CategoricalAggregationFunction](#cfn-quicksight-template-aggregationfunction-categoricalaggregationfunction)" : String,
  "[DateAggregationFunction](#cfn-quicksight-template-aggregationfunction-dateaggregationfunction)" : String,
  "[NumericalAggregationFunction](#cfn-quicksight-template-aggregationfunction-numericalaggregationfunction)" : NumericalAggregationFunction
}
```

### YAML<a name="aws-properties-quicksight-template-aggregationfunction-syntax.yaml"></a>

```
  [CategoricalAggregationFunction](#cfn-quicksight-template-aggregationfunction-categoricalaggregationfunction): String
  [DateAggregationFunction](#cfn-quicksight-template-aggregationfunction-dateaggregationfunction): String
  [NumericalAggregationFunction](#cfn-quicksight-template-aggregationfunction-numericalaggregationfunction): 
    NumericalAggregationFunction
```

## Properties<a name="aws-properties-quicksight-template-aggregationfunction-properties"></a>

`CategoricalAggregationFunction`  <a name="cfn-quicksight-template-aggregationfunction-categoricalaggregationfunction"></a>
Aggregation for categorical values\.  
+  `COUNT`: Aggregate by the total number of values, including duplicates\.
+  `DISTINCT_COUNT`: Aggregate by the total number of distinct values\.
*Required*: No  
*Type*: String  
*Allowed values*: `COUNT | DISTINCT_COUNT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateAggregationFunction`  <a name="cfn-quicksight-template-aggregationfunction-dateaggregationfunction"></a>
Aggregation for date values\.  
+  `COUNT`: Aggregate by the total number of values, including duplicates\.
+  `DISTINCT_COUNT`: Aggregate by the total number of distinct values\.
+  `MIN`: Select the smallest date value\.
+  `MAX`: Select the largest date value\.
*Required*: No  
*Type*: String  
*Allowed values*: `COUNT | DISTINCT_COUNT | MAX | MIN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericalAggregationFunction`  <a name="cfn-quicksight-template-aggregationfunction-numericalaggregationfunction"></a>
Aggregation for numerical values\.  
*Required*: No  
*Type*: [NumericalAggregationFunction](aws-properties-quicksight-template-numericalaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)