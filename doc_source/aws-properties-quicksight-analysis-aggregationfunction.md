# AWS::QuickSight::Analysis AggregationFunction<a name="aws-properties-quicksight-analysis-aggregationfunction"></a>

An aggregation function aggregates values from a dimension or measure\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-aggregationfunction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-aggregationfunction-syntax.json"></a>

```
{
  "[AttributeAggregationFunction](#cfn-quicksight-analysis-aggregationfunction-attributeaggregationfunction)" : AttributeAggregationFunction,
  "[CategoricalAggregationFunction](#cfn-quicksight-analysis-aggregationfunction-categoricalaggregationfunction)" : String,
  "[DateAggregationFunction](#cfn-quicksight-analysis-aggregationfunction-dateaggregationfunction)" : String,
  "[NumericalAggregationFunction](#cfn-quicksight-analysis-aggregationfunction-numericalaggregationfunction)" : NumericalAggregationFunction
}
```

### YAML<a name="aws-properties-quicksight-analysis-aggregationfunction-syntax.yaml"></a>

```
  [AttributeAggregationFunction](#cfn-quicksight-analysis-aggregationfunction-attributeaggregationfunction): 
    AttributeAggregationFunction
  [CategoricalAggregationFunction](#cfn-quicksight-analysis-aggregationfunction-categoricalaggregationfunction): String
  [DateAggregationFunction](#cfn-quicksight-analysis-aggregationfunction-dateaggregationfunction): String
  [NumericalAggregationFunction](#cfn-quicksight-analysis-aggregationfunction-numericalaggregationfunction): 
    NumericalAggregationFunction
```

## Properties<a name="aws-properties-quicksight-analysis-aggregationfunction-properties"></a>

`AttributeAggregationFunction`  <a name="cfn-quicksight-analysis-aggregationfunction-attributeaggregationfunction"></a>
Aggregation for attributes\.  
*Required*: No  
*Type*: [AttributeAggregationFunction](aws-properties-quicksight-analysis-attributeaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoricalAggregationFunction`  <a name="cfn-quicksight-analysis-aggregationfunction-categoricalaggregationfunction"></a>
Aggregation for categorical values\.  
+  `COUNT`: Aggregate by the total number of values, including duplicates\.
+  `DISTINCT_COUNT`: Aggregate by the total number of distinct values\.
*Required*: No  
*Type*: String  
*Allowed values*: `COUNT | DISTINCT_COUNT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateAggregationFunction`  <a name="cfn-quicksight-analysis-aggregationfunction-dateaggregationfunction"></a>
Aggregation for date values\.  
+  `COUNT`: Aggregate by the total number of values, including duplicates\.
+  `DISTINCT_COUNT`: Aggregate by the total number of distinct values\.
+  `MIN`: Select the smallest date value\.
+  `MAX`: Select the largest date value\.
*Required*: No  
*Type*: String  
*Allowed values*: `COUNT | DISTINCT_COUNT | MAX | MIN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericalAggregationFunction`  <a name="cfn-quicksight-analysis-aggregationfunction-numericalaggregationfunction"></a>
Aggregation for numerical values\.  
*Required*: No  
*Type*: [NumericalAggregationFunction](aws-properties-quicksight-analysis-numericalaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)