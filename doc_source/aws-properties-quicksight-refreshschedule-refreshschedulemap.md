# AWS::QuickSight::RefreshSchedule RefreshScheduleMap<a name="aws-properties-quicksight-refreshschedule-refreshschedulemap"></a>

A summary of a configured refresh schedule for a dataset\.

## Syntax<a name="aws-properties-quicksight-refreshschedule-refreshschedulemap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-refreshschedule-refreshschedulemap-syntax.json"></a>

```
{
  "[RefreshType](#cfn-quicksight-refreshschedule-refreshschedulemap-refreshtype)" : String,
  "[ScheduleFrequency](#cfn-quicksight-refreshschedule-refreshschedulemap-schedulefrequency)" : ScheduleFrequency,
  "[ScheduleId](#cfn-quicksight-refreshschedule-refreshschedulemap-scheduleid)" : String,
  "[StartAfterDateTime](#cfn-quicksight-refreshschedule-refreshschedulemap-startafterdatetime)" : String
}
```

### YAML<a name="aws-properties-quicksight-refreshschedule-refreshschedulemap-syntax.yaml"></a>

```
  [RefreshType](#cfn-quicksight-refreshschedule-refreshschedulemap-refreshtype): String
  [ScheduleFrequency](#cfn-quicksight-refreshschedule-refreshschedulemap-schedulefrequency): 
    ScheduleFrequency
  [ScheduleId](#cfn-quicksight-refreshschedule-refreshschedulemap-scheduleid): String
  [StartAfterDateTime](#cfn-quicksight-refreshschedule-refreshschedulemap-startafterdatetime): String
```

## Properties<a name="aws-properties-quicksight-refreshschedule-refreshschedulemap-properties"></a>

`RefreshType`  <a name="cfn-quicksight-refreshschedule-refreshschedulemap-refreshtype"></a>
The type of refresh that a dataset undergoes\. Valid values are as follows:  
+ `FULL_REFRESH`: A complete refresh of a dataset\.
+ `INCREMENTAL_REFRESH`: A partial refresh of some rows of a dataset, based on the time window specified\.
For more information on full and incremental refreshes, see [Refreshing SPICE data](https://docs.aws.amazon.com/quicksight/latest/user/refreshing-imported-data.html) in the *Amazon QuickSight User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleFrequency`  <a name="cfn-quicksight-refreshschedule-refreshschedulemap-schedulefrequency"></a>
The frequency for the refresh schedule\.  
*Required*: No  
*Type*: [ScheduleFrequency](aws-properties-quicksight-refreshschedule-schedulefrequency.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleId`  <a name="cfn-quicksight-refreshschedule-refreshschedulemap-scheduleid"></a>
An identifier for the refresh schedule\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StartAfterDateTime`  <a name="cfn-quicksight-refreshschedule-refreshschedulemap-startafterdatetime"></a>
Time after which the refresh schedule can be started, expressed in `YYYY-MM-DDTHH:MM:SS` format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)