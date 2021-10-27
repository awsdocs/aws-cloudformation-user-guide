# AWS::CloudWatch::MetricStream MetricStreamFilter<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter"></a>

This structure contains the name of one of the metric namespaces that is listed in a filter of a metric stream\. 

## Syntax<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter-syntax.json"></a>

```
{
  "[Namespace](#cfn-cloudwatch-metricstream-metricstreamfilter-namespace)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter-syntax.yaml"></a>

```
  [Namespace](#cfn-cloudwatch-metricstream-metricstreamfilter-namespace): String
```

## Properties<a name="aws-properties-cloudwatch-metricstream-metricstreamfilter-properties"></a>

`Namespace`  <a name="cfn-cloudwatch-metricstream-metricstreamfilter-namespace"></a>
The name of the metric namespace in the filter\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)