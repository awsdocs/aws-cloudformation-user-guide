# AWS::Logs::MetricFilter<a name="aws-resource-logs-metricfilter"></a>

The `AWS::Logs::MetricFilter` resource specifies a metric filter that describes how CloudWatch Logs extracts information from logs and transforms it into Amazon CloudWatch metrics\. If you have multiple metric filters that are associated with a log group, all the filters are applied to the log streams in that group\.

The maximum number of metric filters that can be associated with a log group is 100\.

## Syntax<a name="aws-resource-logs-metricfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-metricfilter-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::MetricFilter",
  "Properties" : {
      "[FilterName](#cfn-logs-metricfilter-filtername)" : String,
      "[FilterPattern](#cfn-logs-metricfilter-filterpattern)" : String,
      "[LogGroupName](#cfn-logs-metricfilter-loggroupname)" : String,
      "[MetricTransformations](#cfn-logs-metricfilter-metrictransformations)" : [ MetricTransformation, ... ]
    }
}
```

### YAML<a name="aws-resource-logs-metricfilter-syntax.yaml"></a>

```
Type: AWS::Logs::MetricFilter
Properties: 
  [FilterName](#cfn-logs-metricfilter-filtername): String
  [FilterPattern](#cfn-logs-metricfilter-filterpattern): String
  [LogGroupName](#cfn-logs-metricfilter-loggroupname): String
  [MetricTransformations](#cfn-logs-metricfilter-metrictransformations): 
    - MetricTransformation
```

## Properties<a name="aws-resource-logs-metricfilter-properties"></a>

`FilterName`  <a name="cfn-logs-metricfilter-filtername"></a>
The name of the metric filter\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[^:*]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FilterPattern`  <a name="cfn-logs-metricfilter-filterpattern"></a>
A filter pattern for extracting metric data out of ingested log events\. For more information, see [Filter and Pattern Syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogGroupName`  <a name="cfn-logs-metricfilter-loggroupname"></a>
The name of an existing log group that you want to associate with this metric filter\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\.\-_/#A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MetricTransformations`  <a name="cfn-logs-metricfilter-metrictransformations"></a>
The metric transformations\.  
*Required*: Yes  
*Type*: List of [MetricTransformation](aws-properties-logs-metricfilter-metrictransformation.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-logs-metricfilter--examples"></a>



### Create a Metric Filter<a name="aws-resource-logs-metricfilter--examples--Create_a_Metric_Filter"></a>

The following example sends a value of `1` to the `404Count` metric whenever the status code field includes a `404` value\.

#### JSON<a name="aws-resource-logs-metricfilter--examples--Create_a_Metric_Filter--json"></a>

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

#### YAML<a name="aws-resource-logs-metricfilter--examples--Create_a_Metric_Filter--yaml"></a>

```
404MetricFilter: 
  Type: AWS::Logs::MetricFilter
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