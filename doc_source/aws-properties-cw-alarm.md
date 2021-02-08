# AWS::CloudWatch::Alarm<a name="aws-properties-cw-alarm"></a>

The `AWS::CloudWatch::Alarm` type specifies an alarm and associates it with the specified metric or metric math expression\.

When this operation creates an alarm, the alarm state is immediately set to `INSUFFICIENT_DATA`\. The alarm is then evaluated and its state is set appropriately\. Any actions associated with the new state are then executed\.

When you update an existing alarm, its state is left unchanged, but the update completely overwrites the previous configuration of the alarm\.



## Syntax<a name="aws-properties-cw-alarm-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cw-alarm-syntax.json"></a>

```
{
  "Type" : "AWS::CloudWatch::Alarm",
  "Properties" : {
      "[ActionsEnabled](#cfn-cloudwatch-alarms-actionsenabled)" : Boolean,
      "[AlarmActions](#cfn-cloudwatch-alarms-alarmactions)" : [ String, ... ],
      "[AlarmDescription](#cfn-cloudwatch-alarms-alarmdescription)" : String,
      "[AlarmName](#cfn-cloudwatch-alarms-alarmname)" : String,
      "[ComparisonOperator](#cfn-cloudwatch-alarms-comparisonoperator)" : String,
      "[DatapointsToAlarm](#cfn-cloudwatch-alarm-datapointstoalarm)" : Integer,
      "[Dimensions](#cfn-cloudwatch-alarms-dimension)" : [ Dimension, ... ],
      "[EvaluateLowSampleCountPercentile](#cfn-cloudwatch-alarms-evaluatelowsamplecountpercentile)" : String,
      "[EvaluationPeriods](#cfn-cloudwatch-alarms-evaluationperiods)" : Integer,
      "[ExtendedStatistic](#cfn-cloudwatch-alarms-extendedstatistic)" : String,
      "[InsufficientDataActions](#cfn-cloudwatch-alarms-insufficientdataactions)" : [ String, ... ],
      "[MetricName](#cfn-cloudwatch-alarms-metricname)" : String,
      "[Metrics](#cfn-cloudwatch-alarm-metrics)" : [ MetricDataQuery, ... ],
      "[Namespace](#cfn-cloudwatch-alarms-namespace)" : String,
      "[OKActions](#cfn-cloudwatch-alarms-okactions)" : [ String, ... ],
      "[Period](#cfn-cloudwatch-alarms-period)" : Integer,
      "[Statistic](#cfn-cloudwatch-alarms-statistic)" : String,
      "[Threshold](#cfn-cloudwatch-alarms-threshold)" : Double,
      "[ThresholdMetricId](#cfn-cloudwatch-alarms-dynamic-threshold)" : String,
      "[TreatMissingData](#cfn-cloudwatch-alarms-treatmissingdata)" : String,
      "[Unit](#cfn-cloudwatch-alarms-unit)" : String
    }
}
```

### YAML<a name="aws-properties-cw-alarm-syntax.yaml"></a>

```
Type: AWS::CloudWatch::Alarm
Properties: 
  [ActionsEnabled](#cfn-cloudwatch-alarms-actionsenabled): Boolean
  [AlarmActions](#cfn-cloudwatch-alarms-alarmactions): 
    - String
  [AlarmDescription](#cfn-cloudwatch-alarms-alarmdescription): String
  [AlarmName](#cfn-cloudwatch-alarms-alarmname): String
  [ComparisonOperator](#cfn-cloudwatch-alarms-comparisonoperator): String
  [DatapointsToAlarm](#cfn-cloudwatch-alarm-datapointstoalarm): Integer
  [Dimensions](#cfn-cloudwatch-alarms-dimension): 
    - Dimension
  [EvaluateLowSampleCountPercentile](#cfn-cloudwatch-alarms-evaluatelowsamplecountpercentile): String
  [EvaluationPeriods](#cfn-cloudwatch-alarms-evaluationperiods): Integer
  [ExtendedStatistic](#cfn-cloudwatch-alarms-extendedstatistic): String
  [InsufficientDataActions](#cfn-cloudwatch-alarms-insufficientdataactions): 
    - String
  [MetricName](#cfn-cloudwatch-alarms-metricname): String
  [Metrics](#cfn-cloudwatch-alarm-metrics): 
    - MetricDataQuery
  [Namespace](#cfn-cloudwatch-alarms-namespace): String
  [OKActions](#cfn-cloudwatch-alarms-okactions): 
    - String
  [Period](#cfn-cloudwatch-alarms-period): Integer
  [Statistic](#cfn-cloudwatch-alarms-statistic): String
  [Threshold](#cfn-cloudwatch-alarms-threshold): Double
  [ThresholdMetricId](#cfn-cloudwatch-alarms-dynamic-threshold): String
  [TreatMissingData](#cfn-cloudwatch-alarms-treatmissingdata): String
  [Unit](#cfn-cloudwatch-alarms-unit): String
```

## Properties<a name="aws-properties-cw-alarm-properties"></a>

`ActionsEnabled`  <a name="cfn-cloudwatch-alarms-actionsenabled"></a>
Indicates whether actions should be executed during any changes to the alarm state\. The default is TRUE\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmActions`  <a name="cfn-cloudwatch-alarms-alarmactions"></a>
The list of actions to execute when this alarm transitions into an ALARM state from any other state\. Specify each action as an Amazon Resource Name \(ARN\)\. For more information about creating alarms and the actions that you can specify, see [PutMetricAlarm](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutMetricAlarm.html) in the *Amazon CloudWatch API Reference*\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmDescription`  <a name="cfn-cloudwatch-alarms-alarmdescription"></a>
The description of the alarm\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AlarmName`  <a name="cfn-cloudwatch-alarms-alarmname"></a>
The name of the alarm\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the alarm name\.   
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ComparisonOperator`  <a name="cfn-cloudwatch-alarms-comparisonoperator"></a>
The arithmetic operation to use when comparing the specified statistic and threshold\. The specified statistic value is used as the first operand\.  
You can specify the following values: `GreaterThanThreshold`, `GreaterThanOrEqualToThreshold`, `LessThanThreshold`, or `LessThanOrEqualToThreshold`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `GreaterThanOrEqualToThreshold | GreaterThanThreshold | GreaterThanUpperThreshold | LessThanLowerOrGreaterThanUpperThreshold | LessThanLowerThreshold | LessThanOrEqualToThreshold | LessThanThreshold`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatapointsToAlarm`  <a name="cfn-cloudwatch-alarm-datapointstoalarm"></a>
The number of datapoints that must be breaching to trigger the alarm\. This is used only if you are setting an "M out of N" alarm\. In that case, this value is the M, and the value that you set for `EvaluationPeriods` is the N value\. For more information, see [Evaluating an Alarm](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html#alarm-evaluation) in the *Amazon CloudWatch User Guide*\.  
If you omit this parameter, CloudWatch uses the same value here that you set for `EvaluationPeriods`, and the alarm goes to alarm state if that many consecutive periods are breaching\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dimensions`  <a name="cfn-cloudwatch-alarms-dimension"></a>
The dimensions for the metric associated with the alarm\. For an alarm based on a math expression, you can't specify `Dimensions`\. Instead, you use `Metrics`\.  
*Required*: No  
*Type*: List of [Dimension](aws-properties-cw-dimension.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EvaluateLowSampleCountPercentile`  <a name="cfn-cloudwatch-alarms-evaluatelowsamplecountpercentile"></a>
Used only for alarms based on percentiles\. If `ignore`, the alarm state does not change during periods with too few data points to be statistically significant\. If `evaluate` or this parameter is not used, the alarm is always evaluated and possibly changes state no matter how many data points are available\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EvaluationPeriods`  <a name="cfn-cloudwatch-alarms-evaluationperiods"></a>
The number of periods over which data is compared to the specified threshold\. If you are setting an alarm that requires that a number of consecutive data points be breaching to trigger the alarm, this value specifies that number\. If you are setting an "M out of N" alarm, this value is the N, and `DatapointsToAlarm` is the M\.  
For more information, see [Evaluating an Alarm](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html#alarm-evaluation) in the *Amazon CloudWatch User Guide*\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtendedStatistic`  <a name="cfn-cloudwatch-alarms-extendedstatistic"></a>
The percentile statistic for the metric associated with the alarm\. Specify a value between p0\.0 and p100\.  
For an alarm based on a metric, you must specify either `Statistic` or `ExtendedStatistic` but not both\.  
For an alarm based on a math expression, you can't specify `ExtendedStatistic`\. Instead, you use `Metrics`\.  
*Required*: No  
*Type*: String  
*Pattern*: `p(\d{1,2}(\.\d{0,2})?|100)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsufficientDataActions`  <a name="cfn-cloudwatch-alarms-insufficientdataactions"></a>
The actions to execute when this alarm transitions to the `INSUFFICIENT_DATA` state from any other state\. Each action is specified as an Amazon Resource Name \(ARN\)\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-cloudwatch-alarms-metricname"></a>
The name of the metric associated with the alarm\. This is required for an alarm based on a metric\. For an alarm based on a math expression, you use `Metrics` instead and you can't specify `MetricName`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metrics`  <a name="cfn-cloudwatch-alarm-metrics"></a>
An array that enables you to create an alarm based on the result of a metric math expression\. Each item in the array either retrieves a metric or performs a math expression\.  
If you specify the `Metrics` parameter, you cannot specify `MetricName`, `Dimensions`, `Period`, `Namespace`, `Statistic`, `ExtendedStatistic`, or `Unit`\.   
*Required*: No  
*Type*: List of [MetricDataQuery](aws-properties-cloudwatch-alarm-metricdataquery.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-cloudwatch-alarms-namespace"></a>
The namespace of the metric associated with the alarm\. This is required for an alarm based on a metric\. For an alarm based on a math expression, you can't specify `Namespace` and you use `Metrics` instead\.  
For a list of namespaces for metrics from AWS services, see [ AWS Services That Publish CloudWatch Metrics\. ](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/aws-services-cloudwatch-metrics.html)  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[^:].*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OKActions`  <a name="cfn-cloudwatch-alarms-okactions"></a>
The actions to execute when this alarm transitions to the `OK` state from any other state\. Each action is specified as an Amazon Resource Name \(ARN\)\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Period`  <a name="cfn-cloudwatch-alarms-period"></a>
The period, in seconds, over which the statistic is applied\. This is required for an alarm based on a metric\. Valid values are 10, 30, 60, and any multiple of 60\.  
For an alarm based on a math expression, you can't specify `Period`, and instead you use the `Metrics` parameter\.  
*Minimum:* 10  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-cloudwatch-alarms-statistic"></a>
The statistic for the metric associated with the alarm, other than percentile\. For percentile statistics, use `ExtendedStatistic`\.  
For an alarm based on a metric, you must specify either `Statistic` or `ExtendedStatistic` but not both\.  
For an alarm based on a math expression, you can't specify `Statistic`\. Instead, you use `Metrics`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Average | Maximum | Minimum | SampleCount | Sum`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Threshold`  <a name="cfn-cloudwatch-alarms-threshold"></a>
The value to compare with the specified statistic\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThresholdMetricId`  <a name="cfn-cloudwatch-alarms-dynamic-threshold"></a>
In an alarm based on an anomaly detection model, this is the ID of the `ANOMALY_DETECTION_BAND` function used as the threshold for the alarm\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TreatMissingData`  <a name="cfn-cloudwatch-alarms-treatmissingdata"></a>
Sets how this alarm is to handle missing data points\. Valid values are `breaching`, `notBreaching`, `ignore`, and `missing`\. For more information, see [ Configuring How CloudWatch Alarms Treat Missing Data](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html#alarms-and-missing-data) in the *Amazon CloudWatch User Guide*\.  
If you omit this parameter, the default behavior of `missing` is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-cloudwatch-alarms-unit"></a>
The unit of the metric associated with the alarm\. Specify this only if you are creating an alarm based on a single metric\. Do not specify this if you are specifying a `Metrics` array\.  
 You can specify the following values: Seconds, Microseconds, Milliseconds, Bytes, Kilobytes, Megabytes, Gigabytes, Terabytes, Bits, Kilobits, Megabits, Gigabits, Terabits, Percent, Count, Bytes/Second, Kilobytes/Second, Megabytes/Second, Gigabytes/Second, Terabytes/Second, Bits/Second, Kilobits/Second, Megabits/Second, Gigabits/Second, Terabits/Second, Count/Second, or None\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Bits | Bits/Second | Bytes | Bytes/Second | Count | Count/Second | Gigabits | Gigabits/Second | Gigabytes | Gigabytes/Second | Kilobits | Kilobits/Second | Kilobytes | Kilobytes/Second | Megabits | Megabits/Second | Megabytes | Megabytes/Second | Microseconds | Milliseconds | None | Percent | Seconds | Terabits | Terabits/Second | Terabytes | Terabytes/Second`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-cw-alarm-return-values"></a>

### Ref<a name="aws-properties-cw-alarm-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the alarm name, such as `TestAlarm`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-cw-alarm-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-cw-alarm-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the CloudWatch alarm, such as `arn:aws:cloudwatch:us-west-2:123456789012:alarm:myCloudWatchAlarm-CPUAlarm-UXMMZK36R55Z`\.

## Examples<a name="aws-properties-cw-alarm--examples"></a>



### Alarm Based on an Anomaly Detector<a name="aws-properties-cw-alarm--examples--Alarm_Based_on_an_Anomaly_Detector"></a>

This example creates an alarm that is based on an anomaly detector\.

#### JSON<a name="aws-properties-cw-alarm--examples--Alarm_Based_on_an_Anomaly_Detector--json"></a>

```
"Resources": {
    "LambdaInvocationsAnomalyDetector": {
       "Type": "AWS::CloudWatch::AnomalyDetector",
       "Properties": {
          "MetricName": "Invocations",
          "Namespace": "AWS/Lambda",
          "Statistic": "Sum"
       }
    },
    "LambdaInvocationsAlarm": {
       "Type": "AWS::CloudWatch::Alarm",
       "Properties": {
          "AlarmDescription": "Lambda invocations",
          "AlarmName": "LambdaInvocationsAlarm",
          "ComparisonOperator": "LessThanLowerOrGreaterThanUpperThreshold",
          "EvaluationPeriods": 1,
          "Metrics": [
             {
                "Expression": "ANOMALY_DETECTION_BAND(m1, 2)",
                "Id": "ad1"
             },
             {
                "Id": "m1",
                "MetricStat": {
                   "Metric": {
                      "MetricName": "Invocations",
                      "Namespace": "AWS/Lambda"
                   },
                   "Period": 86400,
                   "Stat": "Sum"
                }
             }
          ],
          "ThresholdMetricId": "ad1",
          "TreatMissingData": "breaching"
       }
    }
 }
```

#### YAML<a name="aws-properties-cw-alarm--examples--Alarm_Based_on_an_Anomaly_Detector--yaml"></a>

```
Resources:
  LambdaInvocationsAnomalyDetector:
    Type: AWS::CloudWatch::AnomalyDetector
    Properties:
      MetricName: Invocations
      Namespace: AWS/Lambda
      Stat: Sum

  LambdaInvocationsAlarm:
    Type: AWS::CloudWatch::Alarm
    Properties:
      AlarmDescription: Lambda invocations
      AlarmName: LambdaInvocationsAlarm
      ComparisonOperator: LessThanLowerOrGreaterThanUpperThreshold
      EvaluationPeriods: 1
      Metrics:
      - Expression: ANOMALY_DETECTION_BAND(m1, 2)
        Id: ad1
      - Id: m1
        MetricStat:
          Metric:
            MetricName: Invocations
            Namespace: AWS/Lambda
          Period: !!int 86400
          Stat: Sum
      ThresholdMetricId: ad1
      TreatMissingData: breaching
```

## See also<a name="aws-properties-cw-alarm--seealso"></a>
+  [Amazon CloudWatch Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-cloudwatch.html) 

