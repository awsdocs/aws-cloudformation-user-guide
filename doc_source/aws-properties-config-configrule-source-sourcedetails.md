# AWS Config ConfigRule SourceDetails<a name="aws-properties-config-configrule-source-sourcedetails"></a>

`SourceDetails` is a property of the [AWS Config ConfigRule Source](aws-properties-config-configrule-source.md) property that specifies the source and type of event that triggers AWS Config to evaluate your AWS resources\.

## Syntax<a name="w3ab2c21c14d534b5"></a>

### JSON<a name="aws-properties-config-configrule-source-sourcedetails-syntax.json"></a>

```
{
  "[EventSource](#cfn-config-configrule-source-sourcedetail-eventsource)" : String,
  "[MaximumExecutionFrequency](#cfn-config-configrule-source-sourcedetail-maximumexecutionfrequency)" : String,
  "[MessageType](#cfn-config-configrule-source-sourcedetail-messagetype)" : String
}
```

### YAML<a name="aws-properties-config-configrule-source-sourcedetails-syntax.yaml"></a>

```
[EventSource](#cfn-config-configrule-source-sourcedetail-eventsource): String
[MaximumExecutionFrequency](#cfn-config-configrule-source-sourcedetail-maximumexecutionfrequency): String
[MessageType](#cfn-config-configrule-source-sourcedetail-messagetype): String
```

## Properties<a name="w3ab2c21c14d534b7"></a>

`EventSource`  <a name="cfn-config-configrule-source-sourcedetail-eventsource"></a>
The source, such as an AWS service, that generate events, triggering AWS Config to evaluate your AWS resources\.  
*Valid Values*: `aws.config`  
*Required*: Yes  
*Type*: String

`MaximumExecutionFrequency`  <a name="cfn-config-configrule-source-sourcedetail-maximumexecutionfrequency"></a>
The frequency that you want AWS Config to run evaluations for a custom rule with a periodic trigger\. By default, rules with a periodic trigger are evaluated every 24 hours\. If you specify a value for `MaximumExecutionFrequency`, then `MessageType` must use the `ScheduledNotification` value\.  
*Valid values*: `One_Hour`, `Three_Hours`, `Six_Hours`, `Twelve_Hours`, or `TwentyFour_Hours`\.  
*Required*: No  
*Type*: String

`MessageType`  <a name="cfn-config-configrule-source-sourcedetail-messagetype"></a>
The type of Amazon Simple Notification Service \(Amazon SNS\) message that triggers AWS Config to run an evaluation\. For more information, see the [SourceDetail](http://docs.aws.amazon.com/config/latest/APIReference/API_SourceDetail.html) data type in the *AWS Config API Reference*\.  
*Valid Values*: `ConfigurationItemChangeNotification`, `ConfigurationSnapshotDeliveryCompleted`, `ScheduledNotification`, `OversizedConfigurationItemChangeNotification`  
*Required*: Yes  
*Type*: String