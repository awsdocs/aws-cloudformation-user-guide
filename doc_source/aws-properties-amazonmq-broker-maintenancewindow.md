# AWS::AmazonMQ::Broker MaintenanceWindow<a name="aws-properties-amazonmq-broker-maintenancewindow"></a>

The parameters that determine the `WeeklyStartTime` to apply pending updates or patches to the broker\.

## Syntax<a name="aws-properties-amazonmq-broker-maintenancewindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-maintenancewindow-syntax.json"></a>

```
{
  "[DayOfWeek](#cfn-amazonmq-broker-maintenancewindow-dayofweek)" : String,
  "[TimeOfDay](#cfn-amazonmq-broker-maintenancewindow-timeofday)" : String,
  "[TimeZone](#cfn-amazonmq-broker-maintenancewindow-timezone)" : String
}
```

### YAML<a name="aws-properties-amazonmq-broker-maintenancewindow-syntax.yaml"></a>

```
  [DayOfWeek](#cfn-amazonmq-broker-maintenancewindow-dayofweek): String
  [TimeOfDay](#cfn-amazonmq-broker-maintenancewindow-timeofday): String
  [TimeZone](#cfn-amazonmq-broker-maintenancewindow-timezone): String
```

## Properties<a name="aws-properties-amazonmq-broker-maintenancewindow-properties"></a>

`DayOfWeek`  <a name="cfn-amazonmq-broker-maintenancewindow-dayofweek"></a>
The day of the week\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeOfDay`  <a name="cfn-amazonmq-broker-maintenancewindow-timeofday"></a>
The time, in 24\-hour format\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeZone`  <a name="cfn-amazonmq-broker-maintenancewindow-timezone"></a>
The time zone, UTC by default, in either the Country/City format, or the UTC offset format\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)