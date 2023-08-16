# AWS::CloudWatch::MetricStream MetricStreamFilter<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter"></a>

This structure contains a metric namespace and optionally, a list of metric names, to either include in a metric ' stream or exclude from a metric stream\.

A metric stream's filters can include up to 1000 total names\. This limit applies to the sum of namespace names and metric names in the filters\. For example, this could include 10 metric namespace filters with 99 metrics each, or 20 namespace filters with 49 metrics specified in each filter\. 

## Syntax<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter-syntax.json"></a>

```
{
  "[MetricNames](#cfn-cloudwatch-metricstream-metricstreamfilter-metricnames)" : [ String, ... ],
  "[Namespace](#cfn-cloudwatch-metricstream-metricstreamfilter-namespace)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter-syntax.yaml"></a>

```
  [MetricNames](#cfn-cloudwatch-metricstream-metricstreamfilter-metricnames): 
    - String
  [Namespace](#cfn-cloudwatch-metricstream-metricstreamfilter-namespace): String
```

## Properties<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter-properties"></a>

`MetricNames`  <a name="cfn-cloudwatch-metricstream-metricstreamfilter-metricnames"></a>
The names of the metrics to either include or exclude from the metric stream\.  
If you omit this parameter, all metrics in the namespace are included or excluded, depending on whether this filter is specified as an exclude filter or an include filter\.  
Each metric name can contain only ASCII printable characters \(ASCII range 32 through 126\)\. Each metric name must contain at least one non\-whitespace character\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-cloudwatch-metricstream-metricstreamfilter-namespace"></a>
The name of the metric namespace in the filter\.  
The namespace can contain only ASCII printable characters \(ASCII range 32 through 126\)\. It must contain at least one non\-whitespace character\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)