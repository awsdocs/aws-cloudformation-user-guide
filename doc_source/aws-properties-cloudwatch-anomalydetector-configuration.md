# AWS::CloudWatch::AnomalyDetector Configuration<a name="aws-properties-cloudwatch-anomalydetector-configuration"></a>

Specifies details about how the anomaly detection model is to be trained, including time ranges to exclude when training and updating the model\. The configuration can also include the time zone to use for the metric\.

## Syntax<a name="aws-properties-cloudwatch-anomalydetector-configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-anomalydetector-configuration-syntax.json"></a>

```
{
  "[ExcludedTimeRanges](#cfn-cloudwatch-anomalydetector-configuration-excludedtimeranges)" : [ Range, ... ],
  "[MetricTimeZone](#cfn-cloudwatch-anomalydetector-configuration-metrictimezone)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-anomalydetector-configuration-syntax.yaml"></a>

```
  [ExcludedTimeRanges](#cfn-cloudwatch-anomalydetector-configuration-excludedtimeranges): 
    - Range
  [MetricTimeZone](#cfn-cloudwatch-anomalydetector-configuration-metrictimezone): String
```

## Properties<a name="aws-properties-cloudwatch-anomalydetector-configuration-properties"></a>

`ExcludedTimeRanges`  <a name="cfn-cloudwatch-anomalydetector-configuration-excludedtimeranges"></a>
Specifies an array of time ranges to exclude from use when the anomaly detection model is trained and updated\. Use this to make sure that events that could cause unusual values for the metric, such as deployments, aren't used when CloudWatch creates or updates the model\.  
*Required*: No  
*Type*: List of [Range](aws-properties-cloudwatch-anomalydetector-range.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricTimeZone`  <a name="cfn-cloudwatch-anomalydetector-configuration-metrictimezone"></a>
The time zone to use for the metric\. This is useful to enable the model to automatically account for daylight savings time changes if the metric is sensitive to such time changes\.   
To specify a time zone, use the name of the time zone as specified in the standard tz database\. For more information, see [tz database](https://en.wikipedia.org/wiki/Tz_database)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)