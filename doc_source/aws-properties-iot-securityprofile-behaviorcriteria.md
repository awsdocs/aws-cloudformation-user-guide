# AWS::IoT::SecurityProfile BehaviorCriteria<a name="aws-properties-iot-securityprofile-behaviorcriteria"></a>

The criteria by which the behavior is determined to be normal\.

## Syntax<a name="aws-properties-iot-securityprofile-behaviorcriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-securityprofile-behaviorcriteria-syntax.json"></a>

```
{
  "[ComparisonOperator](#cfn-iot-securityprofile-behaviorcriteria-comparisonoperator)" : String,
  "[ConsecutiveDatapointsToAlarm](#cfn-iot-securityprofile-behaviorcriteria-consecutivedatapointstoalarm)" : Integer,
  "[ConsecutiveDatapointsToClear](#cfn-iot-securityprofile-behaviorcriteria-consecutivedatapointstoclear)" : Integer,
  "[DurationSeconds](#cfn-iot-securityprofile-behaviorcriteria-durationseconds)" : Integer,
  "[MlDetectionConfig](#cfn-iot-securityprofile-behaviorcriteria-mldetectionconfig)" : MachineLearningDetectionConfig,
  "[StatisticalThreshold](#cfn-iot-securityprofile-behaviorcriteria-statisticalthreshold)" : StatisticalThreshold,
  "[Value](#cfn-iot-securityprofile-behaviorcriteria-value)" : MetricValue
}
```

### YAML<a name="aws-properties-iot-securityprofile-behaviorcriteria-syntax.yaml"></a>

```
  [ComparisonOperator](#cfn-iot-securityprofile-behaviorcriteria-comparisonoperator): String
  [ConsecutiveDatapointsToAlarm](#cfn-iot-securityprofile-behaviorcriteria-consecutivedatapointstoalarm): Integer
  [ConsecutiveDatapointsToClear](#cfn-iot-securityprofile-behaviorcriteria-consecutivedatapointstoclear): Integer
  [DurationSeconds](#cfn-iot-securityprofile-behaviorcriteria-durationseconds): Integer
  [MlDetectionConfig](#cfn-iot-securityprofile-behaviorcriteria-mldetectionconfig): 
    MachineLearningDetectionConfig
  [StatisticalThreshold](#cfn-iot-securityprofile-behaviorcriteria-statisticalthreshold): 
    StatisticalThreshold
  [Value](#cfn-iot-securityprofile-behaviorcriteria-value): 
    MetricValue
```

## Properties<a name="aws-properties-iot-securityprofile-behaviorcriteria-properties"></a>

`ComparisonOperator`  <a name="cfn-iot-securityprofile-behaviorcriteria-comparisonoperator"></a>
The operator that relates the thing measured \(`metric`\) to the criteria \(containing a `value` or `statisticalThreshold`\)\. Valid operators include:  
+  `string-list`: `in-set` and `not-in-set` 
+  `number-list`: `in-set` and `not-in-set` 
+  `ip-address-list`: `in-cidr-set` and `not-in-cidr-set` 
+  `number`: `less-than`, `less-than-equals`, `greater-than`, and `greater-than-equals` 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConsecutiveDatapointsToAlarm`  <a name="cfn-iot-securityprofile-behaviorcriteria-consecutivedatapointstoalarm"></a>
If a device is in violation of the behavior for the specified number of consecutive datapoints, an alarm occurs\. If not specified, the default is 1\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConsecutiveDatapointsToClear`  <a name="cfn-iot-securityprofile-behaviorcriteria-consecutivedatapointstoclear"></a>
If an alarm has occurred and the offending device is no longer in violation of the behavior for the specified number of consecutive datapoints, the alarm is cleared\. If not specified, the default is 1\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DurationSeconds`  <a name="cfn-iot-securityprofile-behaviorcriteria-durationseconds"></a>
Use this to specify the time duration over which the behavior is evaluated, for those criteria that have a time dimension \(for example, `NUM_MESSAGES_SENT`\)\. For a `statisticalThreshhold` metric comparison, measurements from all devices are accumulated over this time duration before being used to calculate percentiles, and later, measurements from an individual device are also accumulated over this time duration before being given a percentile rank\. Cannot be used with list\-based metric datatypes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MlDetectionConfig`  <a name="cfn-iot-securityprofile-behaviorcriteria-mldetectionconfig"></a>
The confidence level of the detection model\.  
*Required*: No  
*Type*: [MachineLearningDetectionConfig](aws-properties-iot-securityprofile-machinelearningdetectionconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatisticalThreshold`  <a name="cfn-iot-securityprofile-behaviorcriteria-statisticalthreshold"></a>
A statistical ranking \(percentile\)that indicates a threshold value by which a behavior is determined to be in compliance or in violation of the behavior\.  
*Required*: No  
*Type*: [StatisticalThreshold](aws-properties-iot-securityprofile-statisticalthreshold.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iot-securityprofile-behaviorcriteria-value"></a>
The value to be compared with the `metric`\.  
*Required*: No  
*Type*: [MetricValue](aws-properties-iot-securityprofile-metricvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)