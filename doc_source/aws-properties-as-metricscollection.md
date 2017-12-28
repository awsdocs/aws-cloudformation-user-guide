# Auto Scaling AutoScalingGroup MetricsCollection<a name="aws-properties-as-metricscollection"></a>

The `MetricsCollection` is a property of the [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) resource that describes the group metrics that an Auto Scaling group sends to CloudWatch\. These metrics describe the group rather than any of its instances\. For more information, see [EnableMetricsCollection](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_EnableMetricsCollection.html) in the *Auto Scaling API Reference*\.

## Syntax<a name="w3ab2c21c14c81b5"></a>

### JSON<a name="aws-properties-as-metricscollection-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-metricscollection-granularity)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-metricscollection-metrics)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-as-metricscollection-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-metricscollection-granularity): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-metricscollection-metrics):
  - String
```

## Properties<a name="w3ab2c21c14c81b7"></a>

`Granularity`  
The frequency at which Auto Scaling sends aggregated data to CloudWatch\. For example, you can specify `1Minute` to send aggregated data to CloudWatch every minute\.  
*Required: *Yes  
*Type*: String

`Metrics`  
The list of metrics to collect\. If you don't specify any metrics, all metrics are enabled\.  
*Required: *No  
*Type*: List of String values