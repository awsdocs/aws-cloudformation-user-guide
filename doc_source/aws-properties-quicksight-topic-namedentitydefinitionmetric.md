# AWS::QuickSight::Topic NamedEntityDefinitionMetric<a name="aws-properties-quicksight-topic-namedentitydefinitionmetric"></a>

A structure that represents a metric\.

## Syntax<a name="aws-properties-quicksight-topic-namedentitydefinitionmetric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-topic-namedentitydefinitionmetric-syntax.json"></a>

```
{
  "[Aggregation](#cfn-quicksight-topic-namedentitydefinitionmetric-aggregation)" : String,
  "[AggregationFunctionParameters](#cfn-quicksight-topic-namedentitydefinitionmetric-aggregationfunctionparameters)" : {Key: Value, ...}
}
```

### YAML<a name="aws-properties-quicksight-topic-namedentitydefinitionmetric-syntax.yaml"></a>

```
  [Aggregation](#cfn-quicksight-topic-namedentitydefinitionmetric-aggregation): String
  [AggregationFunctionParameters](#cfn-quicksight-topic-namedentitydefinitionmetric-aggregationfunctionparameters): 
    Key: Value
```

## Properties<a name="aws-properties-quicksight-topic-namedentitydefinitionmetric-properties"></a>

`Aggregation`  <a name="cfn-quicksight-topic-namedentitydefinitionmetric-aggregation"></a>
The aggregation of a named entity\. Valid values for this structure are `SUM`, `MIN`, `MAX`, `COUNT`, `AVERAGE`, `DISTINCT_COUNT`, `STDEV`, `STDEVP`, `VAR`, `VARP`, `PERCENTILE`, `MEDIAN`, and `CUSTOM`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AVERAGE | COUNT | CUSTOM | DISTINCT_COUNT | MAX | MEDIAN | MIN | PERCENTILE | STDEV | STDEVP | SUM | VAR | VARP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AggregationFunctionParameters`  <a name="cfn-quicksight-topic-namedentitydefinitionmetric-aggregationfunctionparameters"></a>
The additional parameters for an aggregation function\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)