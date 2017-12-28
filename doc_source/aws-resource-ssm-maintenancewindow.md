# AWS::SSM::MaintenanceWindow<a name="aws-resource-ssm-maintenancewindow"></a>

The `AWS::SSM::MaintenanceWindow` resource represents general information about a Maintenance Window for Amazon EC2 Systems Manager\. Maintenance Windows let you define a schedule for when to perform potentially disruptive actions on your instances—such as patching an operating system \(OS\), updating drivers, or installing software\. Each Maintenance Window has a schedule, a duration, a set of registered targets, and a set of registered tasks\. For more information, see [ Systems Manager Maintenance Windows](http://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-maintenance.html) in the *Amazon EC2 Systems Manager User Guide* and [ CreateMaintenanceWindow](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreateMaintenanceWindow.html) in the *Amazon EC2 Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindow-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindow",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-allowunassociatedtargets)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-cutoff)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-schedule)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-duration)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-name)" : String
  }
}
```

### YAML<a name="aws-resource-ssm-maintenancewindow-syntax.yaml"></a>

```
Type: "AWS::SSM::MaintenanceWindow"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-allowunassociatedtargets): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-cutoff): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-schedule): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-duration): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindow-name): String
```

## Properties<a name="aws-resource-ssm-maintenancewindow-properties"></a>

`Description`  
A description of the Maintenance Window\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`AllowUnassociatedTargets`  
Enables a Maintenance Window task to execute on managed instances, even if you haven't registered those instances as targets\. If this is enabled, then you must specify the unregistered instances \(by instance ID\) when you register a task with the Maintenance Window\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Cutoff`  
The number of hours before the end of the Maintenance Window that Systems Manager stops scheduling new tasks for execution\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: No interruption 

`Schedule`  
The schedule of the Maintenance Window in the form of a cron or rate expression\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Duration`  
The duration of the Maintenance Window in hours\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: No interruption 

`Name`  
The name of the Maintenance Window\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

## Return Values<a name="aws-resource-ssm-maintenancewindow-returnvalues"></a>

### Ref<a name="w3ab2c21c10e1010b9b3"></a>

When you pass the logical ID of an `AWS::SSM::MaintenanceWindow` resource to the intrinsic `Ref` function, the function returns the physical ID of the resource, such as `mw-abcde1234567890yz`\. 

For more information about using the `Ref` function, see Ref\. 

## See Also<a name="aws-resource-ssm-maintenancewindow-seealso"></a>

+ [AWS::SSM::MaintenanceWindowTarget](aws-resource-ssm-maintenancewindowtarget.md)

+ [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md)

+ [ CreateMaintenanceWindow](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreateMaintenanceWindow.html) in the *Amazon EC2 Systems Manager API Reference*