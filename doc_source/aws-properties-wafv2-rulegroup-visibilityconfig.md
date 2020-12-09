# AWS::WAFv2::RuleGroup VisibilityConfig<a name="aws-properties-wafv2-rulegroup-visibilityconfig"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Defines and enables Amazon CloudWatch metrics and web request sample collection\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-visibilityconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-visibilityconfig-syntax.json"></a>

```
{
  "[CloudWatchMetricsEnabled](#cfn-wafv2-rulegroup-visibilityconfig-cloudwatchmetricsenabled)" : Boolean,
  "[MetricName](#cfn-wafv2-rulegroup-visibilityconfig-metricname)" : String,
  "[SampledRequestsEnabled](#cfn-wafv2-rulegroup-visibilityconfig-sampledrequestsenabled)" : Boolean
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-visibilityconfig-syntax.yaml"></a>

```
  [CloudWatchMetricsEnabled](#cfn-wafv2-rulegroup-visibilityconfig-cloudwatchmetricsenabled): Boolean
  [MetricName](#cfn-wafv2-rulegroup-visibilityconfig-metricname): String
  [SampledRequestsEnabled](#cfn-wafv2-rulegroup-visibilityconfig-sampledrequestsenabled): Boolean
```

## Properties<a name="aws-properties-wafv2-rulegroup-visibilityconfig-properties"></a>

`CloudWatchMetricsEnabled`  <a name="cfn-wafv2-rulegroup-visibilityconfig-cloudwatchmetricsenabled"></a>
A boolean indicating whether the associated resource sends metrics to CloudWatch\. For the list of available metrics, see [AWS WAF Metrics](https://docs.aws.amazon.com/waf/latest/developerguide/monitoring-cloudwatch.html#waf-metrics)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-wafv2-rulegroup-visibilityconfig-metricname"></a>
A friendly name of the CloudWatch metric\. The name can contain only alphanumeric characters \(A\-Z, a\-z, 0\-9\), with length from one to 128 characters\. It can't contain whitespace or metric names reserved for AWS WAF, for example "All" and "Default\_Action\." You can't change a `MetricName` after you create a `VisibilityConfig`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[\w#:\.\-/]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SampledRequestsEnabled`  <a name="cfn-wafv2-rulegroup-visibilityconfig-sampledrequestsenabled"></a>
A boolean indicating whether AWS WAF should store a sampling of the web requests that match the rules\. You can view the sampled requests through the AWS WAF console\.   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)