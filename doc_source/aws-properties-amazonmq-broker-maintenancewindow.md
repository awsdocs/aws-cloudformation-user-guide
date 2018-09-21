# Amazon MQ Broker MaintenanceWindow<a name="aws-properties-amazonmq-broker-maintenancewindow"></a>

<a name="aws-properties-amazonmq-broker-maintenancewindow-description"></a>The `MaintenanceWindow` property type specifies the parameters that determine the `WeeklyStartTime` for an Amazon MQ broker\.

<a name="aws-properties-amazonmq-broker-maintenancewindow-inheritance"></a> `MaintenanceWindow` is a property of the `[AWS::AmazonMQ::Broker](aws-resource-amazonmq-broker.md)` resource\.

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
The day of the week, for example `MONDAY`, `TUESDAY`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TimeOfDay`  <a name="cfn-amazonmq-broker-maintenancewindow-timeofday"></a>
The time, in 24\-hour format\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TimeZone`  <a name="cfn-amazonmq-broker-maintenancewindow-timezone"></a>
The time zone, UTC by default, in either the Country/City format, or the UTC offset format\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 