# AWS::CloudWatch::AnomalyDetector MetricMathAnomalyDetector<a name="aws-properties-cloudwatch-anomalydetector-metricmathanomalydetector"></a>

Indicates the CloudWatch math expression that provides the time series the anomaly detector uses as input\. The designated math expression must return a single time series\.

## Syntax<a name="aws-properties-cloudwatch-anomalydetector-metricmathanomalydetector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-anomalydetector-metricmathanomalydetector-syntax.json"></a>

```
{
  "[MetricDataQueries](#cfn-cloudwatch-anomalydetector-metricmathanomalydetector-metricdataqueries)" : [ MetricDataQuery, ... ]
}
```

### YAML<a name="aws-properties-cloudwatch-anomalydetector-metricmathanomalydetector-syntax.yaml"></a>

```
  [MetricDataQueries](#cfn-cloudwatch-anomalydetector-metricmathanomalydetector-metricdataqueries): 
    - MetricDataQuery
```

## Properties<a name="aws-properties-cloudwatch-anomalydetector-metricmathanomalydetector-properties"></a>

`MetricDataQueries`  <a name="cfn-cloudwatch-anomalydetector-metricmathanomalydetector-metricdataqueries"></a>
An array of metric data query structures that enables you to create an anomaly detector based on the result of a metric math expression\. Each item in `MetricDataQueries` gets a metric or performs a math expression\. One item in `MetricDataQueries` is the expression that provides the time series that the anomaly detector uses as input\. Designate the expression by setting `ReturnData` to `true` for this object in the array\. For all other expressions and metrics, set `ReturnData` to `false`\. The designated expression must return a single time series\.  
*Required*: No  
*Type*: [List](aws-properties-cloudwatch-anomalydetector-metricdataqueries.md) of [MetricDataQuery](aws-properties-cloudwatch-anomalydetector-metricdataquery.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)