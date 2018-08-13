# AWS::Logs::MetricFilter<a name="aws-resource-logs-metricfilter"></a>

The `AWS::Logs::MetricFilter` resource creates a metric filter that describes how Amazon CloudWatch Logs extracts information from logs that you specify and transforms it into Amazon CloudWatch metrics\. If you have multiple metric filters that are associated with a log group, all the filters are applied to the log streams in that group\.

**Topics**
+ [Syntax](#aws-resource-logs-metricfilter-syntax)
+ [Properties](#w3ab2c21c10d880b9)
+ [Examples](#w3ab2c21c10d880c11)
+ [Additional Information](#w3ab2c21c10d880c13)

## Syntax<a name="aws-resource-logs-metricfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-metricfilter-syntax.json"></a>

```
{
  "Type": "AWS::Logs::MetricFilter",    
  "Properties": {
    "[FilterPattern](#cfn-cwl-metricfilter-filterpattern)": String,
    "[LogGroupName](#cfn-cwl-metricfilter-loggroupname)": String,
    "[MetricTransformations](#cfn-cwl-metricfilter-metrictransformations)": [ MetricTransformations, ... ]
  }
}
```

### YAML<a name="aws-resource-logs-metricfilter-syntax.yaml"></a>

```
Type: "AWS::Logs::MetricFilter"
Properties: 
  [FilterPattern](#cfn-cwl-metricfilter-filterpattern): String
  [LogGroupName](#cfn-cwl-metricfilter-loggroupname): String
  [MetricTransformations](#cfn-cwl-metricfilter-metrictransformations):
    MetricTransformations
```

## Properties<a name="w3ab2c21c10d880b9"></a>

**Note**  
For more information about constraints and values for each property, see [PutMetricFilter](http://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_PutMetricFilter.html) in the *Amazon CloudWatch Logs API Reference*\.

`FilterPattern`  <a name="cfn-cwl-metricfilter-filterpattern"></a>
Describes the pattern that CloudWatch Logs follows to interpret each entry in a log\. A log entry might contain fields such as timestamps, IP addresses, error codes, bytes transferred, and so on\. You use the pattern to specify those fields and to specify what to look for in the log file\. For example, if you're interested in error codes that begin with `1234`, your filter pattern might be `[timestamps, ip_addresses, error_codes = 1234*, size, ...]`\. For more information, see [ Filter and Pattern Syntax](http://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html#extract-log-event-values) in the *Amazon CloudWatch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LogGroupName`  <a name="cfn-cwl-metricfilter-loggroupname"></a>
The name of an existing log group that you want to associate with this metric filter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`MetricTransformations`  <a name="cfn-cwl-metricfilter-metrictransformations"></a>
Describes how to transform data from a log into a CloudWatch metric\.  
*Required*: Yes  
*Type*: A list of [CloudWatch Logs MetricFilter MetricTransformation Property](aws-properties-logs-metricfilter-metrictransformation.md)  
Currently, you can specify only one metric transformation for each metric filter\. If you want to specify multiple metric transformations, you must specify multiple metric filters\.
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Examples<a name="w3ab2c21c10d880c11"></a>

### <a name="w3ab2c21c10d880c11b2"></a>

The following example sends a value of `1` to the `404Count` metric whenever the status code field includes a `404` value\.

#### JSON<a name="aws-resource-logs-metricfilter-example.json"></a>

```
"404MetricFilter": {
    "Type": "AWS::Logs::MetricFilter",
    "Properties": {
        "LogGroupName": { "Ref": "myLogGroup" },
        "FilterPattern": "[ip, identity, user_id, timestamp, request, status_code = 404, size]",
        "MetricTransformations": [
            {
                "MetricValue": "1",
                "MetricNamespace": "WebServer/404s",
                "MetricName": "404Count"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-logs-metricfilter-example.yaml"></a>

```
404MetricFilter: 
  Type: "AWS::Logs::MetricFilter"
  Properties: 
    LogGroupName: 
      Ref: "myLogGroup"
    FilterPattern: "[ip, identity, user_id, timestamp, request, status_code = 404, size]"
    MetricTransformations: 
      - 
        MetricValue: "1"
        MetricNamespace: "WebServer/404s"
        MetricName: "404Count"
```

## Additional Information<a name="w3ab2c21c10d880c13"></a>

For an additional sample template, see [Amazon CloudWatch Logs Template Snippets](quickref-cloudwatchlogs.md)\.