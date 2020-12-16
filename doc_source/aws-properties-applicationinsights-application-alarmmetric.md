# AWS::ApplicationInsights::Application AlarmMetric<a name="aws-properties-applicationinsights-application-alarmmetric"></a>

The `AWS::ApplicationInsights::Application AlarmMetric` property type defines a metric to monitor for the component\.

## Syntax<a name="aws-properties-applicationinsights-application-alarmmetric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-alarmmetric-syntax.json"></a>

```
{
  "[AlarmMetricName](#cfn-applicationinsights-application-alarmmetric-alarmmetricname)" : String
}
```

### YAML<a name="aws-properties-applicationinsights-application-alarmmetric-syntax.yaml"></a>

```
  [AlarmMetricName](#cfn-applicationinsights-application-alarmmetric-alarmmetricname): String
```

## Properties<a name="aws-properties-applicationinsights-application-alarmmetric-properties"></a>

`AlarmMetricName`  <a name="cfn-applicationinsights-application-alarmmetric-alarmmetricname"></a>
The name of the metric to be monitored for the component\. For metrics supported by Application Insights, see [Logs and metrics supported by Amazon CloudWatch Application Insights](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/appinsights-logs-and-metrics.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)