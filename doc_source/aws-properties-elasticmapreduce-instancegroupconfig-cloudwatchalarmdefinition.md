# Amazon EMR InstanceGroupConfig CloudWatchAlarmDefinition<a name="aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition"></a>

The `CloudWatchAlarmDefinition` property specifies the conditions that trigger an automatic scaling activity\. `CloudWatchAlarmDefinition` is a subproperty of the [Amazon EMR InstanceGroupConfig ScalingTrigger](aws-properties-elasticmapreduce-instancegroupconfig-scalingtrigger.md) property type\.

## Syntax<a name="w3ab2c21c14d991b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-comparisonoperator)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-dimensions)" : [ MetricDimension, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-evaluationperiods)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-metricname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-namespace)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-period)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-statistic)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-threshold)" : Double,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-unit)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-syntax.yaml"></a>

```
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-comparisonoperator): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-dimensions):
    - MetricDimension
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-evaluationperiods): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-metricname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-namespace): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-period): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-statistic): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-threshold): Double
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-unit): String
```

## Properties<a name="w3ab2c21c14d991b7"></a>

`ComparisonOperator`  
Determines how the metric specified by `MetricName` is compared to the value specified by `Threshold`\.  
Valid values: `GREATER_THAN_OR_EQUAL`, `GREATER_THAN`, `LESS_THAN`, or `LESS_THAN_OR_EQUAL`\.  
*Required: *Yes  
*Type*: String

`Dimensions`  
A list of CloudWatch metric dimensions\.  
*Required: *No  
*Type*: List of [Amazon EMR InstanceGroupConfig MetricDimension](aws-properties-elasticmapreduce-instancegroupconfig-metricdimension.md)

`EvaluationPeriods`  
The number of periods, expressed in seconds using the `Period` property, during which the alarm condition must exist before the alarm triggers automatic scaling activity\. The default value is 1\.   
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
The period, in seconds, over which the statistic for applying the metric associated with the alarm is applied\. You specify the statistic in the `Statistic` property\. CloudWatch metrics for Amazon EMR  are emitted every five minutes \(300 seconds\)\.  If  you specify a CloudWatch metric for Amazon EMR, specify 300\.  
*Required: *Yes  
*Type*: Integer

`Statistic`  
The statistic to apply to the metric associated with the alarm\. The default is `AVERAGE`\.  
Valid values: `SAMPLE_COUNT`, `AVERAGE`, `SUM`, `MINIMUM`, and `MAXIMUM`\.  
*Required: *No  
*Type*: String

`Threshold`  
The value against which the specified statistic is compared\.  
*Required: *Yes  
*Type*: Double

`Unit`  
The unit of measure associated with the CloudWatch metric being watched\. Specify the unit specified in the CloudWatch metric\.   
For more information, see [CloudWatchAlarmDefinition](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_CloudWatchAlarmDefinition.html) in the *Amazon EMR API Reference*\.  
*Required: *No  
*Type*: String