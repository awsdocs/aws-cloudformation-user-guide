# AWS::Logs::MetricFilter Dimension<a name="aws-properties-logs-metricfilter-dimension"></a>

Specifies the CloudWatch metric dimensions to publish with this metric\.

 Because dimensions are part of the unique identifier for a metric, whenever a unique dimension name/value pair is extracted from your logs, you are creating a new variation of that metric\.

For more information about publishing dimensions with metrics created by metric filters, see [ Publishing dimensions with metrics from values in JSON or space\-delimited log events](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/FilterAndPatternSyntax.html#logs-metric-filters-dimensions)\.

**Important**  
Metrics extracted from log events are charged as custom metrics\. To prevent unexpected high charges, do not specify high\-cardinality fields such as `IPAddress` or `requestID` as dimensions\. Each different value found for a dimension is treated as a separate metric and accrues charges as a separate custom metric\.   
To help prevent accidental high charges, Amazon disables a metric filter if it generates 1000 different name/value pairs for the dimensions that you have specified within a certain amount of time\.  
You can also set up a billing alarm to alert you if your charges are higher than expected\. For more information, see [ Creating a Billing Alarm to Monitor Your Estimated AWS Charges](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/monitor_estimated_charges_with_cloudwatch.html)\. 

## Syntax<a name="aws-properties-logs-metricfilter-dimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-logs-metricfilter-dimension-syntax.json"></a>

```
{
  "[Key](#cfn-logs-metricfilter-dimension-key)" : String,
  "[Value](#cfn-logs-metricfilter-dimension-value)" : String
}
```

### YAML<a name="aws-properties-logs-metricfilter-dimension-syntax.yaml"></a>

```
  [Key](#cfn-logs-metricfilter-dimension-key): String
  [Value](#cfn-logs-metricfilter-dimension-value): String
```

## Properties<a name="aws-properties-logs-metricfilter-dimension-properties"></a>

`Key`  <a name="cfn-logs-metricfilter-dimension-key"></a>
The name for the CloudWatch metric dimension that the metric filter creates\.  
Dimension names must contain only ASCII characters, must include at least one non\-whitespace character, and cannot start with a colon \(:\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-logs-metricfilter-dimension-value"></a>
The log event field that will contain the value for this dimension\. This dimension will only be published for a metric if the value is found in the log event\. For example, `$.eventType` for JSON log events, or `$server` for space\-delimited log events\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)