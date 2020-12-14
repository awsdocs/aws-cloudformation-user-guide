# AWS::CloudWatch::AnomalyDetector<a name="aws-resource-cloudwatch-anomalydetector"></a>

The `AWS::CloudWatch::AnomalyDetector` type specifies an anomaly detection band for a certain metric and statistic\. The band represents the expected "normal" range for the metric values\. Anomaly detection bands can be used for visualization of a metric's expected values, and for alarms\.

## Syntax<a name="aws-resource-cloudwatch-anomalydetector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudwatch-anomalydetector-syntax.json"></a>

```
{
  "Type" : "AWS::CloudWatch::AnomalyDetector",
  "Properties" : {
      "[Configuration](#cfn-cloudwatch-anomalydetector-configuration)" : Configuration,
      "[Dimensions](#cfn-cloudwatch-anomalydetector-dimensions)" : [ Dimension, ... ],
      "[MetricName](#cfn-cloudwatch-anomalydetector-metricname)" : String,
      "[Namespace](#cfn-cloudwatch-anomalydetector-namespace)" : String,
      "[Stat](#cfn-cloudwatch-anomalydetector-stat)" : String
    }
}
```

### YAML<a name="aws-resource-cloudwatch-anomalydetector-syntax.yaml"></a>

```
Type: AWS::CloudWatch::AnomalyDetector
Properties: 
  [Configuration](#cfn-cloudwatch-anomalydetector-configuration): 
    Configuration
  [Dimensions](#cfn-cloudwatch-anomalydetector-dimensions): 
    - Dimension
  [MetricName](#cfn-cloudwatch-anomalydetector-metricname): String
  [Namespace](#cfn-cloudwatch-anomalydetector-namespace): String
  [Stat](#cfn-cloudwatch-anomalydetector-stat): String
```

## Properties<a name="aws-resource-cloudwatch-anomalydetector-properties"></a>

`Configuration`  <a name="cfn-cloudwatch-anomalydetector-configuration"></a>
Specifies details about how the anomaly detection model is to be trained, including time ranges to exclude when training and updating the model\. The configuration can also include the time zone to use for the metric\.  
*Required*: No  
*Type*: [Configuration](aws-properties-cloudwatch-anomalydetector-configuration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dimensions`  <a name="cfn-cloudwatch-anomalydetector-dimensions"></a>
The dimensions of the metric associated with the anomaly detection band\.  
*Required*: No  
*Type*: List of [Dimension](aws-properties-cloudwatch-anomalydetector-dimension.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MetricName`  <a name="cfn-cloudwatch-anomalydetector-metricname"></a>
The name of the metric associated with the anomaly detection band\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Namespace`  <a name="cfn-cloudwatch-anomalydetector-namespace"></a>
The namespace of the metric associated with the anomaly detection band\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Stat`  <a name="cfn-cloudwatch-anomalydetector-stat"></a>
The statistic of the metric associated with the anomaly detection band\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-cloudwatch-anomalydetector--examples"></a>



### Anomaly Detector<a name="aws-resource-cloudwatch-anomalydetector--examples--Anomaly_Detector"></a>

This example creates an anomaly detector model for the metric named `JvmMetric` with the dimension value of `UsedMemory`\. It excludes a time range from the model training\.

#### JSON<a name="aws-resource-cloudwatch-anomalydetector--examples--Anomaly_Detector--json"></a>

```
{
    "Description": "AnomalyDetectorOnUsedMemory",
    "Resources": {
        "AnomalyDetectorOnUsedMemory": {
            "Type": "AWS::CloudWatch::AnomalyDetector",
            "Properties": {
                "MetricName": "JvmMetric",
                "Namespace": "AWSSDK/Java",
                "Stat": "Average",
                "Dimensions": [
                    {
                        "Name": "Memory",
                        "Value": "UsedMemory"
                    }
                ],
                "Configuration": {
                    "MetricTimeZone": "UTC",
                    "ExcludedTimeRanges": [
                        {
                            "StartTime": "2019-07-01T00:00:00",
                            "EndTime": "2019-07-01T23:59:59"
                        }
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudwatch-anomalydetector--examples--Anomaly_Detector--yaml"></a>

```
Description: AnomalyDetectorOnUsedMemory
Resources:
  AnomalyDetectorOnUsedMemory:
    Type: AWS::CloudWatch::AnomalyDetector
    Properties:
      MetricName: JvmMetric
      Namespace: AWSSDK/Java
      Stat: Average
      Dimensions:
        - Name: Memory
          Value: UsedMemory
      Configuration:
        MetricTimeZone: UTC
        ExcludedTimeRanges:
          - StartTime: 2019-07-01T00:00:00
            EndTime: 2019-07-01T23:59:59
```