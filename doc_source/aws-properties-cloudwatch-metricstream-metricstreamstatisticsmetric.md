# AWS::CloudWatch::MetricStream MetricStreamStatisticsMetric<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsmetric"></a>

A structure that specifies the metric name and namespace for one metric that is going to have additional statistics included in the stream\.

## Syntax<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsmetric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsmetric-syntax.json"></a>

```
{
  "[MetricName](#cfn-cloudwatch-metricstream-metricstreamstatisticsmetric-metricname)" : String,
  "[Namespace](#cfn-cloudwatch-metricstream-metricstreamstatisticsmetric-namespace)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsmetric-syntax.yaml"></a>

```
  [MetricName](#cfn-cloudwatch-metricstream-metricstreamstatisticsmetric-metricname): String
  [Namespace](#cfn-cloudwatch-metricstream-metricstreamstatisticsmetric-namespace): String
```

## Properties<a name="aws-properties-cloudwatch-metricstream-metricstreamstatisticsmetric-properties"></a>

`MetricName`  <a name="cfn-cloudwatch-metricstream-metricstreamstatisticsmetric-metricname"></a>
The name of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-cloudwatch-metricstream-metricstreamstatisticsmetric-namespace"></a>
The namespace of the metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)