# AWS::MediaStore::Container MetricPolicy<a name="aws-properties-mediastore-container-metricpolicy"></a>

The metric policy that is associated with the container\. A metric policy allows AWS Elemental MediaStore to send metrics to Amazon CloudWatch\. In the policy, you must indicate whether you want MediaStore to send container\-level metrics\. You can also include rules to define groups of objects that you want MediaStore to send object\-level metrics for\.

To view examples of how to construct a metric policy for your use case, see [Example Metric Policies](https://docs.aws.amazon.com/mediastore/latest/ug/policies-metric-examples.html)\.

## Syntax<a name="aws-properties-mediastore-container-metricpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediastore-container-metricpolicy-syntax.json"></a>

```
{
  "[ContainerLevelMetrics](#cfn-mediastore-container-metricpolicy-containerlevelmetrics)" : String,
  "[MetricPolicyRules](#cfn-mediastore-container-metricpolicy-metricpolicyrules)" : [ MetricPolicyRule, ... ]
}
```

### YAML<a name="aws-properties-mediastore-container-metricpolicy-syntax.yaml"></a>

```
  [ContainerLevelMetrics](#cfn-mediastore-container-metricpolicy-containerlevelmetrics): String
  [MetricPolicyRules](#cfn-mediastore-container-metricpolicy-metricpolicyrules): 
    - MetricPolicyRule
```

## Properties<a name="aws-properties-mediastore-container-metricpolicy-properties"></a>

`ContainerLevelMetrics`  <a name="cfn-mediastore-container-metricpolicy-containerlevelmetrics"></a>
A setting to enable or disable metrics at the container level\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricPolicyRules`  <a name="cfn-mediastore-container-metricpolicy-metricpolicyrules"></a>
A parameter that holds an array of rules that enable metrics at the object level\. This parameter is optional, but if you choose to include it, you must also include at least one rule\. By default, you can include up to five rules\. You can also [request a quota increase](https://console.aws.amazon.com/servicequotas/home?region=us-east-1#!/services/mediastore/quotas) to allow up to 300 rules per policy\.  
*Required*: No  
*Type*: List of [MetricPolicyRule](aws-properties-mediastore-container-metricpolicyrule.md)  
*Maximum*: `300`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)