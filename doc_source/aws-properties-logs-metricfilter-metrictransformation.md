# CloudWatch Logs MetricFilter MetricTransformation Property<a name="aws-properties-logs-metricfilter-metrictransformation"></a>

`MetricTransformation` is a property of the [AWS::Logs::MetricFilter](aws-resource-logs-metricfilter.md) resource that describes how to transform log streams into a CloudWatch metric\.

## Syntax<a name="w3ab2c21c14d359b5"></a>

### JSON<a name="aws-properties-logs-metricfilter-metrictransformation-syntax.json"></a>

```
{
  "[DefaultValue](#cfn-cwl-metricfilter-metrictransformation-defaultvalue)": Double,    
  "[MetricName](#cfn-cwl-metricfilter-metrictransformation-metricname)": String,
  "[MetricNamespace](#cfn-cwl-metricfilter-metrictransformation-metricnamespace)": String,
  "[MetricValue](#cfn-cwl-metricfilter-metrictransformation-metricvalue)": String
}
```

### YAML<a name="aws-properties-logs-metricfilter-metrictransformation-syntax.yaml"></a>

```
[DefaultValue](#cfn-cwl-metricfilter-metrictransformation-defaultvalue): Double
[MetricName](#cfn-cwl-metricfilter-metrictransformation-metricname): String
[MetricNamespace](#cfn-cwl-metricfilter-metrictransformation-metricnamespace): String
[MetricValue](#cfn-cwl-metricfilter-metrictransformation-metricvalue): String
```

## Properties<a name="w3ab2c21c14d359b7"></a>

**Note**  
For more information about constraints and values for each property, see [MetricTransformation](http://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_MetricTransformation.html) in the *Amazon CloudWatch Logs API Reference*\.

`DefaultValue`  <a name="cfn-cwl-metricfilter-metrictransformation-defaultvalue"></a>
The value to emit when a filter pattern does not match a log event\. This value can be null\.  
*Required*: No  
*Type*: Double

`MetricName`  <a name="cfn-cwl-metricfilter-metrictransformation-metricname"></a>
The name of the CloudWatch metric to which the log information will be published\.  
*Required*: Yes  
*Type*: String

`MetricNamespace`  <a name="cfn-cwl-metricfilter-metrictransformation-metricnamespace"></a>
The destination namespace of the CloudWatch metric\. Namespaces are containers for metrics\. For example, you can add related metrics in the same namespace\.  
*Required*: Yes  
*Type*: String

`MetricValue`  <a name="cfn-cwl-metricfilter-metrictransformation-metricvalue"></a>
The value that is published to the CloudWatch metric\. For example, if you're counting the occurrences of a particular term like `Error`, specify `1` for the metric value\. If you're counting the number of bytes transferred, reference the value that is in the log event by using `$` followed by the name of the field that you specified in the filter pattern, such as `$size`\.  
*Required*: Yes  
*Type*: String

## Examples<a name="w3ab2c21c14d359b9"></a>

### <a name="w3ab2c21c14d359b9b2"></a>

For samples of the `MetricTransformation` property, see [AWS::Logs::MetricFilter](aws-resource-logs-metricfilter.md) or [Amazon CloudWatch Logs Template Snippets](quickref-cloudwatchlogs.md)\.