# AWS IoT TopicRule CloudwatchMetricAction<a name="aws-properties-iot-topicrule-cloudwatchmetricaction"></a>

`CloudwatchMetric` is a property of the `Actions` property that describes an action that captures a CloudWatch metric\.

## Syntax<a name="w3ab2c21c14e1327b5"></a>

### JSON<a name="aws-properties-iot-topicrule-cloudwatchmetricaction-syntax.json"></a>

```
{
  "[MetricName](#cfn-iot-topicrule-cloudwatchmetricaction-metricname)": String,
  "[MetricNamespace](#cfn-iot-topicrule-cloudwatchmetricaction-metricnamespace)": String,
  "[MetricTimestamp](#cfn-iot-topicrule-cloudwatchmetricaction-metrictimestamp)": String,
  "[MetricUnit](#cfn-iot-topicrule-cloudwatchmetricaction-metricunit)": String,
  "[MetricValue](#cfn-iot-topicrule-cloudwatchmetricaction-metricvalue)": String,
  "[RoleArn](#cfn-iot-topicrule-cloudwatchmetricaction-rolearn)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-cloudwatchmetricaction-syntax.yaml"></a>

```
[MetricName](#cfn-iot-topicrule-cloudwatchmetricaction-metricname): String
[MetricNamespace](#cfn-iot-topicrule-cloudwatchmetricaction-metricnamespace): String
[MetricTimestamp](#cfn-iot-topicrule-cloudwatchmetricaction-metrictimestamp): String
[MetricUnit](#cfn-iot-topicrule-cloudwatchmetricaction-metricunit): String
[MetricValue](#cfn-iot-topicrule-cloudwatchmetricaction-metricvalue): String
[RoleArn](#cfn-iot-topicrule-cloudwatchmetricaction-rolearn): String
```

## Properties<a name="w3ab2c21c14e1327b7"></a>

`MetricName`  <a name="cfn-iot-topicrule-cloudwatchmetricaction-metricname"></a>
The name of the CloudWatch metric\.  
*Required*: Yes  
*Type*: String

`MetricNamespace`  <a name="cfn-iot-topicrule-cloudwatchmetricaction-metricnamespace"></a>
The name of the CloudWatch metric namespace\.  
*Required*: Yes  
*Type*: String

`MetricTimestamp`  <a name="cfn-iot-topicrule-cloudwatchmetricaction-metrictimestamp"></a>
An optional [Unix timestamp](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/cloudwatch_concepts.html#about_timestamp)\.  
*Required*: No  
*Type*: String

`MetricUnit`  <a name="cfn-iot-topicrule-cloudwatchmetricaction-metricunit"></a>
The [metric unit](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/cloudwatch_concepts.html#Unit) supported by Amazon CloudWatch\.  
*Required*: Yes  
*Type*: String

`MetricValue`  <a name="cfn-iot-topicrule-cloudwatchmetricaction-metricvalue"></a>
The value to publish to the metric\. For example, if you count the occurrences of a particular term such as `Error`, the value will be `1` for each occurrence\.  
*Required*: Yes  
*Type*: String

`RoleArn`  <a name="cfn-iot-topicrule-cloudwatchmetricaction-rolearn"></a>
The ARN of the IAM role that grants access to the CloudWatch metric\.  
*Required*: Yes  
*Type*: String