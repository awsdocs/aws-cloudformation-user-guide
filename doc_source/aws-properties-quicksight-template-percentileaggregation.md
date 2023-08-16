# AWS::QuickSight::Template PercentileAggregation<a name="aws-properties-quicksight-template-percentileaggregation"></a>

An aggregation based on the percentile of values in a dimension or measure\.

## Syntax<a name="aws-properties-quicksight-template-percentileaggregation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-percentileaggregation-syntax.json"></a>

```
{
  "[PercentileValue](#cfn-quicksight-template-percentileaggregation-percentilevalue)" : Double
}
```

### YAML<a name="aws-properties-quicksight-template-percentileaggregation-syntax.yaml"></a>

```
  [PercentileValue](#cfn-quicksight-template-percentileaggregation-percentilevalue): Double
```

## Properties<a name="aws-properties-quicksight-template-percentileaggregation-properties"></a>

`PercentileValue`  <a name="cfn-quicksight-template-percentileaggregation-percentilevalue"></a>
The percentile value\. This value can be any numeric constant 0–100\. A percentile value of 50 computes the median value of the measure\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)