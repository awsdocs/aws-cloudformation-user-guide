# AWS::IoT::JobTemplate MaintenanceWindow<a name="aws-properties-iot-jobtemplate-maintenancewindow"></a>

An optional configuration within the `SchedulingConfig` to setup a recurring maintenance window with a predetermined start time and duration for the rollout of a job document to all devices in a target group for a job\.

## Syntax<a name="aws-properties-iot-jobtemplate-maintenancewindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-maintenancewindow-syntax.json"></a>

```
{
  "[DurationInMinutes](#cfn-iot-jobtemplate-maintenancewindow-durationinminutes)" : Integer,
  "[StartTime](#cfn-iot-jobtemplate-maintenancewindow-starttime)" : String
}
```

### YAML<a name="aws-properties-iot-jobtemplate-maintenancewindow-syntax.yaml"></a>

```
  [DurationInMinutes](#cfn-iot-jobtemplate-maintenancewindow-durationinminutes): Integer
  [StartTime](#cfn-iot-jobtemplate-maintenancewindow-starttime): String
```

## Properties<a name="aws-properties-iot-jobtemplate-maintenancewindow-properties"></a>

`DurationInMinutes`  <a name="cfn-iot-jobtemplate-maintenancewindow-durationinminutes"></a>
Displays the duration of the next maintenance window\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-iot-jobtemplate-maintenancewindow-starttime"></a>
Displays the start time of the next maintenance window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)