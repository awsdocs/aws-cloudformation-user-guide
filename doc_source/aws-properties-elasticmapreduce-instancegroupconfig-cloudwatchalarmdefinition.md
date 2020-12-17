# AWS::EMR::InstanceGroupConfig CloudWatchAlarmDefinition<a name="aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition"></a>

`CloudWatchAlarmDefinition` is a subproperty of the `ScalingTrigger `property, which determines when to trigger an automatic scaling activity\. Scaling activity begins when you satisfy the defined alarm conditions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-syntax.json"></a>

```
{
  "[ComparisonOperator](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-comparisonoperator)" : String,
  "[Dimensions](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-dimensions)" : [ MetricDimension, ... ],
  "[EvaluationPeriods](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-evaluationperiods)" : Integer,
  "[MetricName](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-metricname)" : String,
  "[Namespace](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-namespace)" : String,
  "[Period](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-period)" : Integer,
  "[Statistic](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-statistic)" : String,
  "[Threshold](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-threshold)" : Double,
  "[Unit](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-unit)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-syntax.yaml"></a>

```
  [ComparisonOperator](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-comparisonoperator): String
  [Dimensions](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-dimensions): 
    - MetricDimension
  [EvaluationPeriods](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-evaluationperiods): Integer
  [MetricName](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-metricname): String
  [Namespace](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-namespace): String
  [Period](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-period): Integer
  [Statistic](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-statistic): String
  [Threshold](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-threshold): Double
  [Unit](#cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-unit): String
```

## Properties<a name="aws-properties-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-properties"></a>

`ComparisonOperator`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-comparisonoperator"></a>
Determines how the metric specified by `MetricName` is compared to the value specified by `Threshold`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `GREATER_THAN | GREATER_THAN_OR_EQUAL | LESS_THAN | LESS_THAN_OR_EQUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dimensions`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-dimensions"></a>
A CloudWatch metric dimension\.  
*Required*: No  
*Type*: List of [MetricDimension](aws-properties-elasticmapreduce-instancegroupconfig-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EvaluationPeriods`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-evaluationperiods"></a>
The number of periods, in five\-minute increments, during which the alarm condition must exist before the alarm triggers automatic scaling activity\. The default value is `1`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-metricname"></a>
The name of the CloudWatch metric that is watched to determine an alarm condition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-namespace"></a>
The namespace for the CloudWatch metric\. The default is `AWS/ElasticMapReduce`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Period`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-period"></a>
The period, in seconds, over which the statistic is applied\. EMR CloudWatch metrics are emitted every five minutes \(300 seconds\), so if an EMR CloudWatch metric is specified, specify `300`\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-statistic"></a>
The statistic to apply to the metric associated with the alarm\. The default is `AVERAGE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AVERAGE | MAXIMUM | MINIMUM | SAMPLE_COUNT | SUM`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Threshold`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-threshold"></a>
The value against which the specified statistic is compared\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-elasticmapreduce-instancegroupconfig-cloudwatchalarmdefinition-unit"></a>
The unit of measure associated with the CloudWatch metric being watched\. The value specified for `Unit` must correspond to the units specified in the CloudWatch metric\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BITS | BITS_PER_SECOND | BYTES | BYTES_PER_SECOND | COUNT | COUNT_PER_SECOND | GIGA_BITS | GIGA_BITS_PER_SECOND | GIGA_BYTES | GIGA_BYTES_PER_SECOND | KILO_BITS | KILO_BITS_PER_SECOND | KILO_BYTES | KILO_BYTES_PER_SECOND | MEGA_BITS | MEGA_BITS_PER_SECOND | MEGA_BYTES | MEGA_BYTES_PER_SECOND | MICRO_SECONDS | MILLI_SECONDS | NONE | PERCENT | SECONDS | TERA_BITS | TERA_BITS_PER_SECOND | TERA_BYTES | TERA_BYTES_PER_SECOND`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)