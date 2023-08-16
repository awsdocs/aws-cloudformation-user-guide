# AWS::QuickSight::RefreshSchedule ScheduleFrequency<a name="aws-properties-quicksight-refreshschedule-schedulefrequency"></a>

The frequency for the refresh schedule\.

## Syntax<a name="aws-properties-quicksight-refreshschedule-schedulefrequency-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-refreshschedule-schedulefrequency-syntax.json"></a>

```
{
  "[Interval](#cfn-quicksight-refreshschedule-schedulefrequency-interval)" : String,
  "[RefreshOnDay](#cfn-quicksight-refreshschedule-schedulefrequency-refreshonday)" : RefreshOnDay,
  "[TimeOfTheDay](#cfn-quicksight-refreshschedule-schedulefrequency-timeoftheday)" : String,
  "[TimeZone](#cfn-quicksight-refreshschedule-schedulefrequency-timezone)" : String
}
```

### YAML<a name="aws-properties-quicksight-refreshschedule-schedulefrequency-syntax.yaml"></a>

```
  [Interval](#cfn-quicksight-refreshschedule-schedulefrequency-interval): String
  [RefreshOnDay](#cfn-quicksight-refreshschedule-schedulefrequency-refreshonday): 
    RefreshOnDay
  [TimeOfTheDay](#cfn-quicksight-refreshschedule-schedulefrequency-timeoftheday): String
  [TimeZone](#cfn-quicksight-refreshschedule-schedulefrequency-timezone): String
```

## Properties<a name="aws-properties-quicksight-refreshschedule-schedulefrequency-properties"></a>

`Interval`  <a name="cfn-quicksight-refreshschedule-schedulefrequency-interval"></a>
The interval between scheduled refreshes\. Valid values are as follows:  
+ `MINUTE15`: The dataset refreshes every 15 minutes\. This value is only supported for incremental refreshes\. This interval can only be used for one schedule per dataset\.
+ `MINUTE30`: The dataset refreshes every 30 minutes\. This value is only supported for incremental refreshes\. This interval can only be used for one schedule per dataset\.
+ `HOURLY`: The dataset refreshes every hour\. This interval can only be used for one schedule per dataset\.
+ `DAILY`: The dataset refreshes every day\.
+ `WEEKLY`: The dataset refreshes every week\.
+ `MONTHLY`: The dataset refreshes every month\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RefreshOnDay`  <a name="cfn-quicksight-refreshschedule-schedulefrequency-refreshonday"></a>
The day of the week that you want to schedule the refresh on\. This value is required for weekly and monthly refresh intervals\.  
*Required*: No  
*Type*: [RefreshOnDay](aws-properties-quicksight-refreshschedule-refreshonday.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeOfTheDay`  <a name="cfn-quicksight-refreshschedule-schedulefrequency-timeoftheday"></a>
The time of day that you want the dataset to refresh\. This value is expressed in HH:MM format\. This field is not required for schedules that refresh hourly\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeZone`  <a name="cfn-quicksight-refreshschedule-schedulefrequency-timezone"></a>
The timezone that you want the refresh schedule to use\. The timezone ID must match a corresponding ID found on `java.util.time.getAvailableIDs()`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)