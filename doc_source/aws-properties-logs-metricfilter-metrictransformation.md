# CloudWatch Logs MetricFilter MetricTransformation Property<a name="aws-properties-logs-metricfilter-metrictransformation"></a>

`MetricTransformation` is a property of the [AWS::Logs::MetricFilter](aws-resource-logs-metricfilter.md) resource that describes how to transform log streams into a CloudWatch metric\.

## Syntax<a name="w3ab2c21c14d287b5"></a>

### JSON<a name="aws-properties-logs-metricfilter-metrictransformation-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cwl-metricfilter-metrictransformation-metricname)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cwl-metricfilter-metrictransformation-metricnamespace)": String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cwl-metricfilter-metrictransformation-metricvalue)": String
}
```

### YAML<a name="aws-properties-logs-metricfilter-metrictransformation-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cwl-metricfilter-metrictransformation-metricname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cwl-metricfilter-metrictransformation-metricnamespace): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cwl-metricfilter-metrictransformation-metricvalue): String
```

## Properties<a name="w3ab2c21c14d287b7"></a>

**Note**  
For more information about constraints and values for each property, see [MetricTransformation](http://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_MetricTransformation.html) in the *Amazon CloudWatch Logs API Reference*\.

`MetricName`  
The name of the CloudWatch metric to which the log information will be published\.  
*Required: *Yes  
*Type*: String

`MetricNamespace`  
The destination namespace of the CloudWatch metric\. Namespaces are containers for metrics\. For example, you can add related metrics in the same namespace\.  
*Required: *Yes  
*Type*: String

`MetricValue`  
The value that is published to the CloudWatch metric\. For example, if you're counting the occurrences of a particular term like `Error`, specify `1` for the metric value\. If you're counting the number of bytes transferred, reference the value that is in the log event by using `$` followed by the name of the field that you specified in the filter pattern, such as `$size`\.  
*Required: *Yes  
*Type*: String

## Examples<a name="w3ab2c21c14d287b9"></a>

### <a name="w3ab2c21c14d287b9b2"></a>

For samples of the `MetricTransformation` property, see [AWS::Logs::MetricFilter](aws-resource-logs-metricfilter.md) or [Amazon CloudWatch Logs Template Snippets](quickref-cloudwatchlogs.md)\.