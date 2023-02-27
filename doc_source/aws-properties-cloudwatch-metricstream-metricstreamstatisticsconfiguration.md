# AWS::CloudWatch::MetricStream MetricStreamStatisticsConfiguration<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsconfiguration"></a>

This structure specifies a list of additional statistics to stream, and the metrics to stream those additional statistics for\.

All metrics that match the combination of metric name and namespace will be streamed with the additional statistics, no matter their dimensions\.

## Syntax<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsconfiguration-syntax.json"></a>

```
{
  "[AdditionalStatistics](#cfn-cloudwatch-metricstream-metricstreamstatisticsconfiguration-additionalstatistics)" : [ String, ... ],
  "[IncludeMetrics](#cfn-cloudwatch-metricstream-metricstreamstatisticsconfiguration-includemetrics)" : [ MetricStreamStatisticsMetric, ... ]
}
```

### YAML<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsconfiguration-syntax.yaml"></a>

```
  [AdditionalStatistics](#cfn-cloudwatch-metricstream-metricstreamstatisticsconfiguration-additionalstatistics): 
    - String
  [IncludeMetrics](#cfn-cloudwatch-metricstream-metricstreamstatisticsconfiguration-includemetrics): 
    - MetricStreamStatisticsMetric
```

## Properties<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsconfiguration-properties"></a>

`AdditionalStatistics`  <a name="cfn-cloudwatch-metricstream-metricstreamstatisticsconfiguration-additionalstatistics"></a>
The additional statistics to stream for the metrics listed in `IncludeMetrics`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeMetrics`  <a name="cfn-cloudwatch-metricstream-metricstreamstatisticsconfiguration-includemetrics"></a>
An array that defines the metrics that are to have additional statistics streamed\.  
*Required*: Yes  
*Type*: List of [MetricStreamStatisticsMetric](aws-properties-cloudwatch-metricstream-metricstreamstatisticsmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)