# AWS::CloudWatch::Alarm<a name="aws-properties-cw-alarm"></a>

The `AWS::CloudWatch::Alarm` type creates a CloudWatch alarm\.

This type supports updates\. For more information about updating this resource, see [PutMetricAlarm](http://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutMetricAlarm.html)\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.

**Topics**
+ [Syntax](#aws-resource-cw-alarm-syntax)
+ [Properties](#aws-properties-cw-alarm-prop)
+ [Return Values](#aws-properties-cw-alarm-ref)
+ [Examples](#w3ab2c21c10d233c15)

## Syntax<a name="aws-resource-cw-alarm-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cw-alarm-syntax.json"></a>

```
{
   "Type" : "AWS::CloudWatch::Alarm",
   "Properties" : {
      "[ActionsEnabled](#cfn-cloudwatch-alarms-actionsenabled)" : Boolean,
      "[AlarmActions](#cfn-cloudwatch-alarms-alarmactions)" : [ String, ... ],
      "[AlarmDescription](#cfn-cloudwatch-alarms-alarmdescription)" : String,
      "[AlarmName](#cfn-cloudwatch-alarms-alarmname)" : String,
      "[ComparisonOperator](#cfn-cloudwatch-alarms-comparisonoperator)" : String,
      "[Dimensions](#cfn-cloudwatch-alarms-dimensions)" : [ Dimension, ... ],
      "[EvaluateLowSampleCountPercentile](#cfn-cloudwatch-alarms-evaluatelowsamplecountpercentile)" : String,
      "[EvaluationPeriods](#cfn-cloudwatch-alarms-evaluationperiods)" : Integer,
      "[ExtendedStatistic](#cfn-cloudwatch-alarms-extendedstatistic)" : String,
      "[InsufficientDataActions](#cfn-cloudwatch-alarms-insufficientdataactions)" : [ String, ... ],
      "[MetricName](#cfn-cloudwatch-alarms-metricname)" : String,
      "[Namespace](#cfn-cloudwatch-alarms-namespace)" : String,
      "[OKActions](#cfn-cloudwatch-alarms-okactions)" : [ String, ... ],
      "[Period](#cfn-cloudwatch-alarms-period)" : Integer,
      "[Statistic](#cfn-cloudwatch-alarms-statistic)" : String,
      "[Threshold](#cfn-cloudwatch-alarms-threshold)" : Double,
      "[TreatMissingData](#cfn-cloudwatch-alarms-treatmissingdata)" : String,
      "[Unit](#cfn-cloudwatch-alarms-unit)" : String
   }
}
```

### YAML<a name="aws-resource-cw-alarm-syntax.yaml"></a>

```
Type: "AWS::CloudWatch::Alarm"
Properties:
  [ActionsEnabled](#cfn-cloudwatch-alarms-actionsenabled): Boolean
  [AlarmActions](#cfn-cloudwatch-alarms-alarmactions):
    - String
  [AlarmDescription](#cfn-cloudwatch-alarms-alarmdescription): String
  [AlarmName](#cfn-cloudwatch-alarms-alarmname): String
  [ComparisonOperator](#cfn-cloudwatch-alarms-comparisonoperator): String
  [Dimensions](#cfn-cloudwatch-alarms-dimensions):
    - Dimension
  [EvaluateLowSampleCountPercentile](#cfn-cloudwatch-alarms-evaluatelowsamplecountpercentile): String
  [EvaluationPeriods](#cfn-cloudwatch-alarms-evaluationperiods): Integer
  [ExtendedStatistic](#cfn-cloudwatch-alarms-extendedstatistic): String
  [InsufficientDataActions](#cfn-cloudwatch-alarms-insufficientdataactions):
    - String
  [MetricName](#cfn-cloudwatch-alarms-metricname): String
  [Namespace](#cfn-cloudwatch-alarms-namespace): String
  [OKActions](#cfn-cloudwatch-alarms-okactions):
    - String
  [Period](#cfn-cloudwatch-alarms-period): Integer
  [Statistic](#cfn-cloudwatch-alarms-statistic): String
  [Threshold](#cfn-cloudwatch-alarms-threshold): Double
  [TreatMissingData](#cfn-cloudwatch-alarms-treatmissingdata): String
  [Unit](#cfn-cloudwatch-alarms-unit): String
```

## Properties<a name="aws-properties-cw-alarm-prop"></a>

`ActionsEnabled`  <a name="cfn-cloudwatch-alarms-actionsenabled"></a>
Indicates whether actions should be executed during changes to the CloudWatch alarm's state\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AlarmActions`  <a name="cfn-cloudwatch-alarms-alarmactions"></a>
The list of actions to execute when this alarm transitions into an ALARM state from any other state\. Specify each action as an Amazon Resource Name \(ARN\)\. For more information about creating alarms and the actions that you can specify, see [PutMetricAlarm](http://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutMetricAlarm.html) in the *Amazon CloudWatch API Reference* and [Creating Amazon CloudWatch Alarms](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/AlarmThatSendsEmail.html) in the *Amazon CloudWatch User Guide*\.  
For Auto Scaling scaling polices, you can specify only one policy\. If you associate more than one policy, Amazon CloudWatch executes only the first scaling policy\.
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AlarmDescription`  <a name="cfn-cloudwatch-alarms-alarmdescription"></a>
The description of the alarm\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AlarmName`  <a name="cfn-cloudwatch-alarms-alarmname"></a>
A name for the alarm\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the alarm name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ComparisonOperator`  <a name="cfn-cloudwatch-alarms-comparisonoperator"></a>
The arithmetic operation to use when comparing the specified `Statistic` and `Threshold`\. AWS CloudFormation uses the value of `Statistic` as the first operand\.  
You can specify the following values: `GreaterThanOrEqualToThreshold` , `GreaterThanThreshold`, `LessThanThreshold`, or `LessThanOrEqualToThreshold`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Dimensions`  <a name="cfn-cloudwatch-alarms-dimensions"></a>
The dimensions of the metric for the alarm\.  
*Required*: No  
*Type*: List of [Metric Dimension](aws-properties-cw-dimension.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EvaluateLowSampleCountPercentile`  <a name="cfn-cloudwatch-alarms-evaluatelowsamplecountpercentile"></a>
Used only for alarms that are based on percentiles\. Specifies whether to evaluate the data and potentially change the alarm state if there are too few data points to be statistically significant\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EvaluationPeriods`  <a name="cfn-cloudwatch-alarms-evaluationperiods"></a>
The number of periods over which data is compared to the specified threshold\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ExtendedStatistic`  <a name="cfn-cloudwatch-alarms-extendedstatistic"></a>
The percentile statistic for the metric\. Specify a value between p0\.0 and p100\.  
*Required*: Conditional\. You must specify either the `ExtendedStatistic` or the `Statistic` property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InsufficientDataActions`  <a name="cfn-cloudwatch-alarms-insufficientdataactions"></a>
The list of actions to execute when this alarm transitions into an INSUFFICIENT\_DATA state\. Specify each action as an Amazon Resource Number \(ARN\)\. Currently, the only action supported is publishing to an Amazon SNS topic or an Auto Scaling policy\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MetricName`  <a name="cfn-cloudwatch-alarms-metricname"></a>
The name of the metric associated with the alarm\. For more information about the metrics that you can specify, see [Amazon CloudWatch Namespaces, Dimensions, and Metrics Reference](http://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/CW_Support_For_AWS.html) in the *Amazon CloudWatch User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Namespace`  <a name="cfn-cloudwatch-alarms-namespace"></a>
The namespace of the metric that is associated with the alarm\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`OKActions`  <a name="cfn-cloudwatch-alarms-okactions"></a>
The list of actions to execute when this alarm transitions into an OK state\. Specify each action as an Amazon Resource Number \(ARN\)\. Currently, the only action supported is publishing to an SNS topic or an Auto Scaling policy\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Period`  <a name="cfn-cloudwatch-alarms-period"></a>
The time over which the specified statistic is applied\. Specify time in seconds, in multiples of 60\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Statistic`  <a name="cfn-cloudwatch-alarms-statistic"></a>
The statistic to apply to the alarm's associated metric\.  
You can specify the following values: `SampleCount`, `Average`, `Sum`, `Minimum`, or `Maximum`\.  
*Required*: Conditional\. You must specify either the `ExtendedStatistic` or the `Statistic` property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Threshold`  <a name="cfn-cloudwatch-alarms-threshold"></a>
The value against which the specified statistic is compared\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TreatMissingData`  <a name="cfn-cloudwatch-alarms-treatmissingdata"></a>
Sets how this alarm is to handle missing data points\. If `TreatMissingData` is omitted, the default behavior of `missing` is used\. For more information, see [PutMetricAlarm](http://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutMetricAlarm.html) in the *Amazon CloudWatch API Reference* and [Configuring How CloudWatch Alarms Treats Missing Data](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html#alarms-and-missing-data) in the *Amazon CloudWatch User Guide*\.   
*Valid values*: `breaching`, `notBreaching`, `ignore`, `missing`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Unit`  <a name="cfn-cloudwatch-alarms-unit"></a>
The unit for the metric that is associated with the alarm\.  
You can specify the following values: Seconds, Microseconds, Milliseconds, Bytes, Kilobytes, Megabytes, Gigabytes , Terabytes, Bits, Kilobits, Megabits, Gigabits, Terabits,\| Percent , Count,Bytes/Second , Kilobytes/Second, Megabytes/Second, Gigabytes/Second, Terabytes/Second , Bits/Second, Kilobits/Second , Megabits/Second , Gigabits/Second , Terabits/Second, Count/Second , or None\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-properties-cw-alarm-ref"></a>

### Ref<a name="w3ab2c21c10d233c13b2"></a>

When you specify an `AWS::CloudWatch::Alarm` type as an argument to the `Ref` function, AWS CloudFormation returns the value of the `AlarmName`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-properties-cw-alarm-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the CloudWatch alarm, such as `arn:aws:cloudwatch:us-east-2:123456789012:alarm:myCloudWatchAlarm-CPUAlarm-UXMMZK36R55Z`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d233c15"></a>

For examples, see [Amazon CloudWatch Template Snippets](quickref-cloudwatch.md)\.