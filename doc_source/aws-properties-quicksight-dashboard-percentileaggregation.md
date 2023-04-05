# AWS::QuickSight::Dashboard PercentileAggregation<a name="aws-properties-quicksight-dashboard-percentileaggregation"></a>

An aggregation based on the percentile of values in a dimension or measure\.

## Syntax<a name="aws-properties-quicksight-dashboard-percentileaggregation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-percentileaggregation-syntax.json"></a>

```
{
  "[PercentileValue](#cfn-quicksight-dashboard-percentileaggregation-percentilevalue)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-percentileaggregation-syntax.yaml"></a>

```
  [PercentileValue](#cfn-quicksight-dashboard-percentileaggregation-percentilevalue): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-percentileaggregation-properties"></a>

`PercentileValue`  <a name="cfn-quicksight-dashboard-percentileaggregation-percentilevalue"></a>
The percentile value\. This value can be any numeric constant 0–100\. A percentile value of 50 computes the median value of the measure\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)