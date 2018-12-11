# AWS::SSM::MaintenanceWindow<a name="aws-resource-ssm-maintenancewindow"></a>

The `AWS::SSM::MaintenanceWindow` resource represents general information about a Maintenance Window for AWS Systems Manager\. Maintenance Windows let you define a schedule for when to perform potentially disruptive actions on your instances—such as patching an operating system \(OS\), updating drivers, or installing software\. Each Maintenance Window has a schedule, a duration, a set of registered targets, and a set of registered tasks\. For more information, see [ Systems Manager Maintenance Windows](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-maintenance.html) in the *AWS Systems Manager User Guide* and [ CreateMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreateMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindow-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindow",
  "Properties" : {
    "[Name](#cfn-ssm-maintenancewindow-name)" : String,
    "[Description](#cfn-ssm-maintenancewindow-description)" : String,
    "[AllowUnassociatedTargets](#cfn-ssm-maintenancewindow-allowunassociatedtargets)" : Boolean,
    "[Schedule](#cfn-ssm-maintenancewindow-schedule)" : String,
    "[Duration](#cfn-ssm-maintenancewindow-duration)" : Integer,
    "[Cutoff](#cfn-ssm-maintenancewindow-cutoff)" : Integer,
    "[StartDate](#cfn-ssm-maintenancewindow-startdate)" : String,,
    "[EndDate](#cfn-ssm-maintenancewindow-enddate)" : String,,
    "[ScheduleTimezone](#cfn-ssm-maintenancewindow-scheduletimezone)" : String
  }
}
```

### YAML<a name="aws-resource-ssm-maintenancewindow-syntax.yaml"></a>

```
Type: "AWS::SSM::MaintenanceWindow"
Properties:
  [Name](#cfn-ssm-maintenancewindow-name): String
  [Description](#cfn-ssm-maintenancewindow-description): String
  [AllowUnassociatedTargets](#cfn-ssm-maintenancewindow-allowunassociatedtargets): Boolean
  [Schedule](#cfn-ssm-maintenancewindow-schedule): String
  [Duration](#cfn-ssm-maintenancewindow-duration): Integer
  [Cutoff](#cfn-ssm-maintenancewindow-cutoff): Integer
  [StartDate](#cfn-ssm-maintenancewindow-startdate): String
  [EndDate](#cfn-ssm-maintenancewindow-enddate): String
  [ScheduleTimezone](#cfn-ssm-maintenancewindow-scheduletimezone): String
```

## Properties<a name="aws-resource-ssm-maintenancewindow-properties"></a>

`Name`  <a name="cfn-ssm-maintenancewindow-name"></a>
The name of the Maintenance Window\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-ssm-maintenancewindow-description"></a>
A description of the Maintenance Window\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AllowUnassociatedTargets`  <a name="cfn-ssm-maintenancewindow-allowunassociatedtargets"></a>
Enables a Maintenance Window task to execute on managed instances, even if you haven't registered those instances as targets\. If this is enabled, then you must specify the unregistered instances \(by instance ID\) when you register a task with the Maintenance Window\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Schedule`  <a name="cfn-ssm-maintenancewindow-schedule"></a>
The schedule of the Maintenance Window in the form of a cron or rate expression\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Duration`  <a name="cfn-ssm-maintenancewindow-duration"></a>
The duration of the Maintenance Window in hours\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Cutoff`  <a name="cfn-ssm-maintenancewindow-cutoff"></a>
The number of hours before the end of the Maintenance Window that Systems Manager stops scheduling new tasks for execution\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StartDate`  <a name="cfn-ssm-maintenancewindow-startdate"></a>
The date and time, in ISO\-8601 Extended format, for when you want the Maintenance Window to become active\. StartDate allows you to delay activation of the Maintenance Window until the specified future date\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`EndDate`  <a name="cfn-ssm-maintenancewindow-enddate"></a>
The date and time, in ISO\-8601 Extended format, for when you want the Maintenance Window to become inactive\. EndDate allows you to set a date and time in the future when the Maintenance Window will no longer run\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ScheduleTimezone`  <a name="cfn-ssm-maintenancewindow-scheduletimezone"></a>
The time zone that the scheduled Maintenance Window executions are based on, in Internet Assigned Numbers Authority \(IANA\) format\. For example: "America/Los\_Angeles", "etc/UTC", or "Asia/Seoul"\. For more information, see the [Time Zone Database](https://www.iana.org/time-zones) on the IANA website\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-ssm-maintenancewindow-returnvalues"></a>

### Ref<a name="w4ab1c21c10d207c19b9b3"></a>

When you pass the logical ID of an `AWS::SSM::MaintenanceWindow` resource to the intrinsic `Ref` function, the function returns the maintenance window ID, such as `mw-abcde1234567890yz`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## See Also<a name="aws-resource-ssm-maintenancewindow-seealso"></a>
+ [AWS::SSM::MaintenanceWindowTarget](aws-resource-ssm-maintenancewindowtarget.md)
+ [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md)
+ [ CreateMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreateMaintenanceWindow.html) in the *AWS Systems Manager API Reference*