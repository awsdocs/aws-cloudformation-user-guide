# Amazon EMR Cluster CloudWatchAlarmDefinition<a name="aws-properties-elasticmapreduce-cluster-cloudwatchalarmdefinition"></a>

`CloudWatchAlarmDefinition` is a subproperty of the [Amazon EMR Cluster ScalingTrigger](aws-properties-elasticmapreduce-cluster-scalingtrigger.md) property, which determines when to trigger an automatic scaling activity\. Scaling activity begins when you satisfy the defined alarm conditions\.

## Syntax<a name="w3ab2c21c14d882b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-cluster-cloudwatchalarmdefinition-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-comparisonoperator)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-dimensions)" : [ MetricDimension, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-evaluationperiods)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-metricname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-namespace)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-period)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-statistic)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-threshold)" : Double,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-unit)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-cloudwatchalarmdefinition-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-comparisonoperator): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-dimensions): 
    - MetricDimension
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-evaluationperiods): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-metricname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-namespace): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-period): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-statistic): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-threshold): Double
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-cluster-scalingtrigger-cloudwatchalarmdefinition-unit): String
```

## Properties<a name="w3ab2c21c14d882b7"></a>

`ComparisonOperator`  
Determines how the metric specified by `MetricName` is compared to the value specified by `Threshold`\.  
Valid values: `GREATER_THAN_OR_EQUAL`, `GREATER_THAN`, `LESS_THAN`, or `LESS_THAN_OR_EQUAL`\.  
*Required: *Yes  
*Type*: String

`Dimensions`  
A list of CloudWatch metric dimensions\.  
*Required: *No  
*Type*: List of [Amazon EMR Cluster MetricDimension](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig-autoscalingpolicy-constraints-scalingrule-scalingtrigger-cloudwatchalarmdefinition-metricdimension.md)

`EvaluationPeriods`  
The number of periods, expressed in seconds using `Period`, during which the alarm condition must exist before the alarm triggers automatic scaling activity\. The default value is 1\.   
*Required: *No  
*Type*: Integer

`MetricName`  
The name of the CloudWatch metric that is watched to determine an alarm condition\.  
*Required: *Yes  
*Type*: String

`Namespace`  
The namespace for the CloudWatch metric\. The default is `AWS/ElasticMapReduce`\.  
*Required: *No  
*Type*: String

`Period`  
The period, in seconds, over which the statistic is applied\. EMR CloudWatch metrics are emitted every five minutes \(300 seconds\), so if an EMR CloudWatch metric is specified, specify 300\.  
*Required: *Yes  
*Type*: Integer

`Statistic`  
The statistic to apply to the metric associated with the alarm\. The default is `AVERAGE`\.  
Valid values: `SAMPLE_COUNT`, `AVERAGE`, `SUM`, `MINIMUM`, or `MAXIMUM`\.  
*Required: *No  
*Type*: String

`Threshold`  
The value against which the specified statistic is compared\.  
*Required: *Yes  
*Type*: Double

`Unit`  
The unit of measure associated with the CloudWatch metric being watched\. The value specified for Unit must correspond to the units specified in the CloudWatch metric\.   
For more information, see [CloudWatchAlarmDefinition](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_CloudWatchAlarmDefinition.html) in the *Amazon Elastic MapReduce Documentation API Reference*\.  
*Required: *No  
*Type*: String