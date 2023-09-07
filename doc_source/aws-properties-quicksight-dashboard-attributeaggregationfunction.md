# AWS::QuickSight::Dashboard AttributeAggregationFunction<a name="aws-properties-quicksight-dashboard-attributeaggregationfunction"></a>

Aggregation for attributes\.

## Syntax<a name="aws-properties-quicksight-dashboard-attributeaggregationfunction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-attributeaggregationfunction-syntax.json"></a>

```
{
  "[SimpleAttributeAggregation](#cfn-quicksight-dashboard-attributeaggregationfunction-simpleattributeaggregation)" : String,
  "[ValueForMultipleValues](#cfn-quicksight-dashboard-attributeaggregationfunction-valueformultiplevalues)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-attributeaggregationfunction-syntax.yaml"></a>

```
  [SimpleAttributeAggregation](#cfn-quicksight-dashboard-attributeaggregationfunction-simpleattributeaggregation): String
  [ValueForMultipleValues](#cfn-quicksight-dashboard-attributeaggregationfunction-valueformultiplevalues): String
```

## Properties<a name="aws-properties-quicksight-dashboard-attributeaggregationfunction-properties"></a>

`SimpleAttributeAggregation`  <a name="cfn-quicksight-dashboard-attributeaggregationfunction-simpleattributeaggregation"></a>
The built\-in aggregation functions for attributes\.  
+  `UNIQUE_VALUE`: Returns the unique value for a field, aggregated by the dimension fields\.
*Required*: No  
*Type*: String  
*Allowed values*: `UNIQUE_VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueForMultipleValues`  <a name="cfn-quicksight-dashboard-attributeaggregationfunction-valueformultiplevalues"></a>
Used by the `UNIQUE_VALUE` aggregation function\. If there are multiple values for the field used by the aggregation, the value for this property will be returned instead\. Defaults to '\*'\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)