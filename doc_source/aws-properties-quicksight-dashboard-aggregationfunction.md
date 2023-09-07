# AWS::QuickSight::Dashboard AggregationFunction<a name="aws-properties-quicksight-dashboard-aggregationfunction"></a>

An aggregation function aggregates values from a dimension or measure\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-aggregationfunction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-aggregationfunction-syntax.json"></a>

```
{
  "[AttributeAggregationFunction](#cfn-quicksight-dashboard-aggregationfunction-attributeaggregationfunction)" : AttributeAggregationFunction,
  "[CategoricalAggregationFunction](#cfn-quicksight-dashboard-aggregationfunction-categoricalaggregationfunction)" : String,
  "[DateAggregationFunction](#cfn-quicksight-dashboard-aggregationfunction-dateaggregationfunction)" : String,
  "[NumericalAggregationFunction](#cfn-quicksight-dashboard-aggregationfunction-numericalaggregationfunction)" : NumericalAggregationFunction
}
```

### YAML<a name="aws-properties-quicksight-dashboard-aggregationfunction-syntax.yaml"></a>

```
  [AttributeAggregationFunction](#cfn-quicksight-dashboard-aggregationfunction-attributeaggregationfunction): 
    AttributeAggregationFunction
  [CategoricalAggregationFunction](#cfn-quicksight-dashboard-aggregationfunction-categoricalaggregationfunction): String
  [DateAggregationFunction](#cfn-quicksight-dashboard-aggregationfunction-dateaggregationfunction): String
  [NumericalAggregationFunction](#cfn-quicksight-dashboard-aggregationfunction-numericalaggregationfunction): 
    NumericalAggregationFunction
```

## Properties<a name="aws-properties-quicksight-dashboard-aggregationfunction-properties"></a>

`AttributeAggregationFunction`  <a name="cfn-quicksight-dashboard-aggregationfunction-attributeaggregationfunction"></a>
Aggregation for attributes\.  
*Required*: No  
*Type*: [AttributeAggregationFunction](aws-properties-quicksight-dashboard-attributeaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoricalAggregationFunction`  <a name="cfn-quicksight-dashboard-aggregationfunction-categoricalaggregationfunction"></a>
Aggregation for categorical values\.  
+  `COUNT`: Aggregate by the total number of values, including duplicates\.
+  `DISTINCT_COUNT`: Aggregate by the total number of distinct values\.
*Required*: No  
*Type*: String  
*Allowed values*: `COUNT | DISTINCT_COUNT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateAggregationFunction`  <a name="cfn-quicksight-dashboard-aggregationfunction-dateaggregationfunction"></a>
Aggregation for date values\.  
+  `COUNT`: Aggregate by the total number of values, including duplicates\.
+  `DISTINCT_COUNT`: Aggregate by the total number of distinct values\.
+  `MIN`: Select the smallest date value\.
+  `MAX`: Select the largest date value\.
*Required*: No  
*Type*: String  
*Allowed values*: `COUNT | DISTINCT_COUNT | MAX | MIN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumericalAggregationFunction`  <a name="cfn-quicksight-dashboard-aggregationfunction-numericalaggregationfunction"></a>
Aggregation for numerical values\.  
*Required*: No  
*Type*: [NumericalAggregationFunction](aws-properties-quicksight-dashboard-numericalaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)