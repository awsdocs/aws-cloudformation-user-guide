# AWS::LookoutMetrics::AnomalyDetector Metric<a name="aws-properties-lookoutmetrics-anomalydetector-metric"></a>

A calculation made by contrasting a measure and a dimension from your source data\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-metric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-metric-syntax.json"></a>

```
{
  "[AggregationFunction](#cfn-lookoutmetrics-anomalydetector-metric-aggregationfunction)" : String,
  "[MetricName](#cfn-lookoutmetrics-anomalydetector-metric-metricname)" : String,
  "[Namespace](#cfn-lookoutmetrics-anomalydetector-metric-namespace)" : String
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-metric-syntax.yaml"></a>

```
  [AggregationFunction](#cfn-lookoutmetrics-anomalydetector-metric-aggregationfunction): String
  [MetricName](#cfn-lookoutmetrics-anomalydetector-metric-metricname): String
  [Namespace](#cfn-lookoutmetrics-anomalydetector-metric-namespace): String
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-metric-properties"></a>

`AggregationFunction`  <a name="cfn-lookoutmetrics-anomalydetector-metric-aggregationfunction"></a>
The function with which the metric is calculated\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-lookoutmetrics-anomalydetector-metric-metricname"></a>
The name of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-lookoutmetrics-anomalydetector-metric-namespace"></a>
The namespace for the metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)