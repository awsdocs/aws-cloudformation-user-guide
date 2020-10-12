# AWS::ApplicationInsights::Application SubComponentConfigurationDetails<a name="aws-properties-applicationinsights-application-subcomponentconfigurationdetails"></a>

The `AWS::ApplicationInsights::Application SubComponentConfigurationDetails` property type specifies the configuration settings of the sub\-components\.

## Syntax<a name="aws-properties-applicationinsights-application-subcomponentconfigurationdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-subcomponentconfigurationdetails-syntax.json"></a>

```
{
  "[AlarmMetrics](#cfn-applicationinsights-application-subcomponentconfigurationdetails-alarmmetrics)" : [ AlarmMetric, ... ],
  "[Logs](#cfn-applicationinsights-application-subcomponentconfigurationdetails-logs)" : [ Log, ... ],
  "[WindowsEvents](#cfn-applicationinsights-application-subcomponentconfigurationdetails-windowsevents)" : [ WindowsEvent, ... ]
}
```

### YAML<a name="aws-properties-applicationinsights-application-subcomponentconfigurationdetails-syntax.yaml"></a>

```
  [AlarmMetrics](#cfn-applicationinsights-application-subcomponentconfigurationdetails-alarmmetrics): 
    - AlarmMetric
  [Logs](#cfn-applicationinsights-application-subcomponentconfigurationdetails-logs): 
    - Log
  [WindowsEvents](#cfn-applicationinsights-application-subcomponentconfigurationdetails-windowsevents): 
    - WindowsEvent
```

## Properties<a name="aws-properties-applicationinsights-application-subcomponentconfigurationdetails-properties"></a>

`AlarmMetrics`  <a name="cfn-applicationinsights-application-subcomponentconfigurationdetails-alarmmetrics"></a>
A list of metrics to monitor for the component\. All component types can use `AlarmMetrics`\.   
*Required*: No  
*Type*: List of [AlarmMetric](aws-properties-applicationinsights-application-alarmmetric.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logs`  <a name="cfn-applicationinsights-application-subcomponentconfigurationdetails-logs"></a>
A list of logs to monitor for the component\. Only Amazon EC2 instances can use `Logs`\.  
*Required*: No  
*Type*: List of [Log](aws-properties-applicationinsights-application-log.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WindowsEvents`  <a name="cfn-applicationinsights-application-subcomponentconfigurationdetails-windowsevents"></a>
A list of Windows Events to monitor for the component\. Only Amazon EC2 instances running on Windows can use `WindowsEvents`\.  
*Required*: No  
*Type*: List of [WindowsEvent](aws-properties-applicationinsights-application-windowsevent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)