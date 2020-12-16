# AWS::Pinpoint::Campaign Schedule<a name="aws-properties-pinpoint-campaign-schedule"></a>

Specifies the schedule settings for a campaign\.

## Syntax<a name="aws-properties-pinpoint-campaign-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-schedule-syntax.json"></a>

```
{
  "[EndTime](#cfn-pinpoint-campaign-schedule-endtime)" : String,
  "[EventFilter](#cfn-pinpoint-campaign-schedule-eventfilter)" : CampaignEventFilter,
  "[Frequency](#cfn-pinpoint-campaign-schedule-frequency)" : String,
  "[IsLocalTime](#cfn-pinpoint-campaign-schedule-islocaltime)" : Boolean,
  "[QuietTime](#cfn-pinpoint-campaign-schedule-quiettime)" : QuietTime,
  "[StartTime](#cfn-pinpoint-campaign-schedule-starttime)" : String,
  "[TimeZone](#cfn-pinpoint-campaign-schedule-timezone)" : String
}
```

### YAML<a name="aws-properties-pinpoint-campaign-schedule-syntax.yaml"></a>

```
  [EndTime](#cfn-pinpoint-campaign-schedule-endtime): String
  [EventFilter](#cfn-pinpoint-campaign-schedule-eventfilter): 
    CampaignEventFilter
  [Frequency](#cfn-pinpoint-campaign-schedule-frequency): String
  [IsLocalTime](#cfn-pinpoint-campaign-schedule-islocaltime): Boolean
  [QuietTime](#cfn-pinpoint-campaign-schedule-quiettime): 
    QuietTime
  [StartTime](#cfn-pinpoint-campaign-schedule-starttime): String
  [TimeZone](#cfn-pinpoint-campaign-schedule-timezone): String
```

## Properties<a name="aws-properties-pinpoint-campaign-schedule-properties"></a>

`EndTime`  <a name="cfn-pinpoint-campaign-schedule-endtime"></a>
The scheduled time, in ISO 8601 format, when the campaign ended or will end\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventFilter`  <a name="cfn-pinpoint-campaign-schedule-eventfilter"></a>
The type of event that causes the campaign to be sent, if the value of the `Frequency` property is `EVENT`\.  
*Required*: No  
*Type*: [CampaignEventFilter](aws-properties-pinpoint-campaign-campaigneventfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Frequency`  <a name="cfn-pinpoint-campaign-schedule-frequency"></a>
Specifies how often the campaign is sent or whether the campaign is sent in response to a specific event\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsLocalTime`  <a name="cfn-pinpoint-campaign-schedule-islocaltime"></a>
Specifies whether the start and end times for the campaign schedule use each recipient's local time\. To base the schedule on each recipient's local time, set this value to `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QuietTime`  <a name="cfn-pinpoint-campaign-schedule-quiettime"></a>
The default quiet time for the campaign\. Quiet time is a specific time range when a campaign doesn't send messages to endpoints, if all the following conditions are met:  
+ The `EndpointDemographic.Timezone` property of the endpoint is set to a valid value\.
+ The current time in the endpoint's time zone is later than or equal to the time specified by the `QuietTime.Start` property for the campaign\.
+ The current time in the endpoint's time zone is earlier than or equal to the time specified by the `QuietTime.End` property for the campaign\.
If any of the preceding conditions isn't met, the endpoint will receive messages from the campaign, even if quiet time is enabled\.  
*Required*: No  
*Type*: [QuietTime](aws-properties-pinpoint-campaign-schedule-quiettime.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-pinpoint-campaign-schedule-starttime"></a>
The scheduled time when the campaign began or will begin\. Valid values are: `IMMEDIATE`, to start the campaign immediately; or, a specific time in ISO 8601 format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeZone`  <a name="cfn-pinpoint-campaign-schedule-timezone"></a>
The starting UTC offset for the campaign schedule, if the value of the `IsLocalTime` property is `true`\. Valid values are: `UTC, UTC+01, UTC+02, UTC+03, UTC+03:30, UTC+04, UTC+04:30, UTC+05, UTC+05:30, UTC+05:45, UTC+06, UTC+06:30, UTC+07, UTC+08, UTC+09, UTC+09:30, UTC+10, UTC+10:30, UTC+11, UTC+12, UTC+13, UTC-02, UTC-03, UTC-04, UTC-05, UTC-06, UTC-07, UTC-08, UTC-09, UTC-10,` and `UTC-11`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)