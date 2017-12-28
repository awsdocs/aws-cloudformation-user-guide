# AWS IoT TopicRule CloudwatchMetricAction<a name="aws-properties-iot-topicrule-cloudwatchmetricaction"></a>

`CloudwatchMetric` is a property of the `Actions` property that describes an action that captures a CloudWatch metric\.

## Syntax<a name="w3ab2c21c14e1130b5"></a>

### JSON<a name="aws-properties-iot-topicrule-cloudwatchmetricaction-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metricname)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metricnamespace)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metrictimestamp)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metricunit)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metricvalue)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-rolearn)": String
}
```

### YAML<a name="aws-properties-iot-topicrule-cloudwatchmetricaction-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metricname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metricnamespace): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metrictimestamp): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metricunit): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-metricvalue): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-cloudwatchmetricaction-rolearn): String
```

## Properties<a name="w3ab2c21c14e1130b7"></a>

`MetricName`  
The name of the CloudWatch metric\.  
*Required: *Yes  
*Type*: String

`MetricNamespace`  
The name of the CloudWatch metric namespace\.  
*Required: *Yes  
*Type*: String

`MetricTimestamp`  
An optional [Unix timestamp](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/cloudwatch_concepts.html#about_timestamp)\.  
*Required: *No  
*Type*: String

`MetricUnit`  
The [metric unit](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/cloudwatch_concepts.html#Unit) supported by Amazon CloudWatch\.  
*Required: *Yes  
*Type*: String

`MetricValue`  
The value to publish to the metric\. For example, if you count the occurrences of a particular term such as `Error`, the value will be `1` for each occurrence\.  
*Required: *Yes  
*Type*: String

`RoleArn`  
The ARN of the IAM role that grants access to the CloudWatch metric\.  
*Required: *Yes  
*Type*: String