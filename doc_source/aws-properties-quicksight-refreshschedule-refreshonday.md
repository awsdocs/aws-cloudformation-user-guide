# AWS::QuickSight::RefreshSchedule RefreshOnDay<a name="aws-properties-quicksight-refreshschedule-refreshonday"></a>

The day that you want yout dataset to refresh\.

## Syntax<a name="aws-properties-quicksight-refreshschedule-refreshonday-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-refreshschedule-refreshonday-syntax.json"></a>

```
{
  "[DayOfMonth](#cfn-quicksight-refreshschedule-refreshonday-dayofmonth)" : String,
  "[DayOfWeek](#cfn-quicksight-refreshschedule-refreshonday-dayofweek)" : String
}
```

### YAML<a name="aws-properties-quicksight-refreshschedule-refreshonday-syntax.yaml"></a>

```
  [DayOfMonth](#cfn-quicksight-refreshschedule-refreshonday-dayofmonth): String
  [DayOfWeek](#cfn-quicksight-refreshschedule-refreshonday-dayofweek): String
```

## Properties<a name="aws-properties-quicksight-refreshschedule-refreshonday-properties"></a>

`DayOfMonth`  <a name="cfn-quicksight-refreshschedule-refreshonday-dayofmonth"></a>
The day of the month that you want your dataset to refresh\. This value is required for monthly refresh intervals\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DayOfWeek`  <a name="cfn-quicksight-refreshschedule-refreshonday-dayofweek"></a>
The day of the week that you want to schedule the refresh on\. This value is required for weekly and monthly refresh intervals\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)