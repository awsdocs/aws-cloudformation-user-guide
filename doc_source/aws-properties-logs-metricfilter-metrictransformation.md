# AWS::Logs::MetricFilter MetricTransformation<a name="aws-properties-logs-metricfilter-metrictransformation"></a>

 `MetricTransformation` is a property of the `AWS::Logs::MetricFilter` resource that describes how to transform log streams into a CloudWatch metric\.

## Syntax<a name="aws-properties-logs-metricfilter-metrictransformation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-logs-metricfilter-metrictransformation-syntax.json"></a>

```
{
  "[DefaultValue](#cfn-cwl-metricfilter-metrictransformation-defaultvalue)" : Double,
  "[MetricName](#cfn-cwl-metricfilter-metrictransformation-metricname)" : String,
  "[MetricNamespace](#cfn-cwl-metricfilter-metrictransformation-metricnamespace)" : String,
  "[MetricValue](#cfn-cwl-metricfilter-metrictransformation-metricvalue)" : String
}
```

### YAML<a name="aws-properties-logs-metricfilter-metrictransformation-syntax.yaml"></a>

```
  [DefaultValue](#cfn-cwl-metricfilter-metrictransformation-defaultvalue): Double
  [MetricName](#cfn-cwl-metricfilter-metrictransformation-metricname): String
  [MetricNamespace](#cfn-cwl-metricfilter-metrictransformation-metricnamespace): String
  [MetricValue](#cfn-cwl-metricfilter-metrictransformation-metricvalue): String
```

## Properties<a name="aws-properties-logs-metricfilter-metrictransformation-properties"></a>

`DefaultValue`  <a name="cfn-cwl-metricfilter-metrictransformation-defaultvalue"></a>
\(Optional\) The value to emit when a filter pattern does not match a log event\. This value can be null\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-cwl-metricfilter-metrictransformation-metricname"></a>
The name of the CloudWatch metric\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricNamespace`  <a name="cfn-cwl-metricfilter-metrictransformation-metricnamespace"></a>
A custom namespace to contain your metric in CloudWatch\. Use namespaces to group together metrics that are similar\. For more information, see [Namespaces](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html#Namespace)\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `[^:*$]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricValue`  <a name="cfn-cwl-metricfilter-metrictransformation-metricvalue"></a>
The value that is published to the CloudWatch metric\. For example, if you're counting the occurrences of a particular term like `Error`, specify 1 for the metric value\. If you're counting the number of bytes transferred, reference the value that is in the log event by using $ followed by the name of the field that you specified in the filter pattern, such as `$size`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)