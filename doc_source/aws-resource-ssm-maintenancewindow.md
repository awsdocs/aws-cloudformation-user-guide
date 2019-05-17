# AWS::SSM::MaintenanceWindow<a name="aws-resource-ssm-maintenancewindow"></a>

The `AWS::SSM::MaintenanceWindow` resource represents general information about a Maintenance Window for AWS Systems Manager\. Maintenance Windows let you define a schedule for when to perform potentially disruptive actions on your instances, such as patching an operating system \(OS\), updating drivers, or installing software\. Each Maintenance Window has a schedule, a duration, a set of registered targets, and a set of registered tasks\. 

For more information, see [Systems Manager Maintenance Windows](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-maintenance.html) in the *AWS Systems Manager User Guide* and [ CreateMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreateMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindow-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindow",
  "Properties" : {
      "[AllowUnassociatedTargets](#cfn-ssm-maintenancewindow-allowunassociatedtargets)" : Boolean,
      "[Cutoff](#cfn-ssm-maintenancewindow-cutoff)" : Integer,
      "[Description](#cfn-ssm-maintenancewindow-description)" : String,
      "[Duration](#cfn-ssm-maintenancewindow-duration)" : Integer,
      "[EndDate](#cfn-ssm-maintenancewindow-enddate)" : String,
      "[Name](#cfn-ssm-maintenancewindow-name)" : String,
      "[Schedule](#cfn-ssm-maintenancewindow-schedule)" : String,
      "[ScheduleTimezone](#cfn-ssm-maintenancewindow-scheduletimezone)" : String,
      "[StartDate](#cfn-ssm-maintenancewindow-startdate)" : String,
      "[Tags](#cfn-ssm-maintenancewindow-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ssm-maintenancewindow-syntax.yaml"></a>

```
Type: AWS::SSM::MaintenanceWindow
Properties: 
  [AllowUnassociatedTargets](#cfn-ssm-maintenancewindow-allowunassociatedtargets): Boolean
  [Cutoff](#cfn-ssm-maintenancewindow-cutoff): Integer
  [Description](#cfn-ssm-maintenancewindow-description): String
  [Duration](#cfn-ssm-maintenancewindow-duration): Integer
  [EndDate](#cfn-ssm-maintenancewindow-enddate): String
  [Name](#cfn-ssm-maintenancewindow-name): String
  [Schedule](#cfn-ssm-maintenancewindow-schedule): String
  [ScheduleTimezone](#cfn-ssm-maintenancewindow-scheduletimezone): String
  [StartDate](#cfn-ssm-maintenancewindow-startdate): String
  [Tags](#cfn-ssm-maintenancewindow-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ssm-maintenancewindow-properties"></a>

`AllowUnassociatedTargets`  <a name="cfn-ssm-maintenancewindow-allowunassociatedtargets"></a>
Enables a Maintenance Window task to run on managed instances, even if you have not registered those instances as targets\. If enabled, then you must specify the unregistered instances \(by instance ID\) when you register a task with the Maintenance Window   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cutoff`  <a name="cfn-ssm-maintenancewindow-cutoff"></a>
The number of hours before the end of the maintenance window that Systems Manager stops scheduling new tasks for execution\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `23`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ssm-maintenancewindow-description"></a>
A description of the maintenance window\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Duration`  <a name="cfn-ssm-maintenancewindow-duration"></a>
The duration of the maintenance window in hours\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `24`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndDate`  <a name="cfn-ssm-maintenancewindow-enddate"></a>
The date and time, in ISO\-8601 Extended format, for when the maintenance window is scheduled to become inactive\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssm-maintenancewindow-name"></a>
The name of the maintenance window\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-ssm-maintenancewindow-schedule"></a>
The schedule of the maintenance window in the form of a cron or rate expression\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleTimezone`  <a name="cfn-ssm-maintenancewindow-scheduletimezone"></a>
The time zone that the scheduled maintenance window executions are based on, in Internet Assigned Numbers Authority \(IANA\) format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartDate`  <a name="cfn-ssm-maintenancewindow-startdate"></a>
The date and time, in ISO\-8601 Extended format, for when the Maintenance Window is scheduled to become active\. StartDate allows you to delay activation of the Maintenance Window until the specified future date\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ssm-maintenancewindow-tags"></a>
Optional metadata that you assign to a resource in the form of an arbitrary set of tags \(key\-value pairs\)\. Tags enable you to categorize a resource in different ways, such as by purpose, owner, or environment\. For example, you might want to tag a Maintenance Window to identify the type of tasks it will run, the types of targets, and the environment it will run in\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-ssm-maintenancewindow-return-values"></a>

### Ref<a name="aws-resource-ssm-maintenancewindow-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Maintenance Window ID, such as `mw-abcde1234567890yz`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-ssm-maintenancewindow--seealso"></a>
+  [AWS::SSM::MaintenanceWindowTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtarget.html) 
+  [AWS::SSM::MaintenanceWindowTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtask.html) 
+  [CreateMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreateMaintenanceWindow.html) in the *AWS Systems Manager API Reference* 