# AWS::QuickSight::Analysis AttributeAggregationFunction<a name="aws-properties-quicksight-analysis-attributeaggregationfunction"></a>

Aggregation for attributes\.

## Syntax<a name="aws-properties-quicksight-analysis-attributeaggregationfunction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-attributeaggregationfunction-syntax.json"></a>

```
{
  "[SimpleAttributeAggregation](#cfn-quicksight-analysis-attributeaggregationfunction-simpleattributeaggregation)" : String,
  "[ValueForMultipleValues](#cfn-quicksight-analysis-attributeaggregationfunction-valueformultiplevalues)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-attributeaggregationfunction-syntax.yaml"></a>

```
  [SimpleAttributeAggregation](#cfn-quicksight-analysis-attributeaggregationfunction-simpleattributeaggregation): String
  [ValueForMultipleValues](#cfn-quicksight-analysis-attributeaggregationfunction-valueformultiplevalues): String
```

## Properties<a name="aws-properties-quicksight-analysis-attributeaggregationfunction-properties"></a>

`SimpleAttributeAggregation`  <a name="cfn-quicksight-analysis-attributeaggregationfunction-simpleattributeaggregation"></a>
The built\-in aggregation functions for attributes\.  
+  `UNIQUE_VALUE`: Returns the unique value for a field, aggregated by the dimension fields\.
*Required*: No  
*Type*: String  
*Allowed values*: `UNIQUE_VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueForMultipleValues`  <a name="cfn-quicksight-analysis-attributeaggregationfunction-valueformultiplevalues"></a>
Used by the `UNIQUE_VALUE` aggregation function\. If there are multiple values for the field used by the aggregation, the value for this property will be returned instead\. Defaults to '\*'\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)