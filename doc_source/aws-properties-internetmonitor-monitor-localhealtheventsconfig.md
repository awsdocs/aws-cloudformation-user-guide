# AWS::InternetMonitor::Monitor LocalHealthEventsConfig<a name="aws-properties-internetmonitor-monitor-localhealtheventsconfig"></a>

Configuration information that determines the threshold and other conditions for when Internet Monitor creates a health event for a local performance or availability issue, when scores cross a threshold for one or more city\-networks\.

Defines the percentages, for performance scores or availability scores, that are the local thresholds for when Amazon CloudWatch Internet Monitor creates a health event\. Also defines whether a local threshold is enabled or disabled, and the minimum percentage of overall traffic that must be impacted by an issue before Internet Monitor creates an event when a threshold is crossed for a local health score\.

If you don't set a local health event threshold, the default value is 60%\.

For more information, see [ Change health event thresholds](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-IM-overview.html#IMUpdateThresholdFromOverview) in the Internet Monitor section of the *Amazon CloudWatch User Guide*\.

## Syntax<a name="aws-properties-internetmonitor-monitor-localhealtheventsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-internetmonitor-monitor-localhealtheventsconfig-syntax.json"></a>

```
{
  "[HealthScoreThreshold](#cfn-internetmonitor-monitor-localhealtheventsconfig-healthscorethreshold)" : Double,
  "[MinTrafficImpact](#cfn-internetmonitor-monitor-localhealtheventsconfig-mintrafficimpact)" : Double,
  "[Status](#cfn-internetmonitor-monitor-localhealtheventsconfig-status)" : String
}
```

### YAML<a name="aws-properties-internetmonitor-monitor-localhealtheventsconfig-syntax.yaml"></a>

```
  [HealthScoreThreshold](#cfn-internetmonitor-monitor-localhealtheventsconfig-healthscorethreshold): Double
  [MinTrafficImpact](#cfn-internetmonitor-monitor-localhealtheventsconfig-mintrafficimpact): Double
  [Status](#cfn-internetmonitor-monitor-localhealtheventsconfig-status): String
```

## Properties<a name="aws-properties-internetmonitor-monitor-localhealtheventsconfig-properties"></a>

`HealthScoreThreshold`  <a name="cfn-internetmonitor-monitor-localhealtheventsconfig-healthscorethreshold"></a>
The health event threshold percentage set for a local health score\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinTrafficImpact`  <a name="cfn-internetmonitor-monitor-localhealtheventsconfig-mintrafficimpact"></a>
The minimum percentage of overall traffic for an application that must be impacted by an issue before Internet Monitor creates an event when a threshold is crossed for a local health score\.  
If you don't set a minimum traffic impact threshold, the default value is 0\.01%\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-internetmonitor-monitor-localhealtheventsconfig-status"></a>
The status of whether Internet Monitor creates a health event based on a threshold percentage set for a local health score\. The status can be `ENABLED` or `DISABLED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)