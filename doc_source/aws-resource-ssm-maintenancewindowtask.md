# AWS::SSM::MaintenanceWindowTask<a name="aws-resource-ssm-maintenancewindowtask"></a>

The `AWS::SSM::MaintenanceWindowTask` resource defines information about a task for a Maintenance Window for AWS Systems Manager\. For more information, see [ RegisterTaskWithMaintenanceWindow](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindowtask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindowtask-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindowTask",
  "Properties" : {
    "[MaxErrors](#cfn-ssm-maintenancewindowtask-maxerrors)" : String,
    "[Description](#cfn-ssm-maintenancewindowtask-description)" : String,
    "[ServiceRoleArn](#cfn-ssm-maintenancewindowtask-servicerolearn)" : String,
    "[Priority](#cfn-ssm-maintenancewindowtask-priority)" : Integer,
    "[MaxConcurrency](#cfn-ssm-maintenancewindowtask-maxconcurrency)" : String,
    "[Targets](#cfn-ssm-maintenancewindowtask-targets)" : [ [*Target*](aws-properties-ssm-maintenancewindowtask-target.md), ... ],
    "[Name](#cfn-ssm-maintenancewindowtask-name)" : String,
    "[TaskArn](#cfn-ssm-maintenancewindowtask-taskarn)" : String,
    "[TaskInvocationParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters)" : [*TaskInvocationParameters*](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md),
    "[WindowId](#cfn-ssm-maintenancewindowtask-windowid)" : String,
    "[TaskParameters](#cfn-ssm-maintenancewindowtask-taskparameters)" : JSON object,
    "[TaskType](#cfn-ssm-maintenancewindowtask-tasktype)" : String,
    "[LoggingInfo](#cfn-ssm-maintenancewindowtask-logginginfo)" : [*LoggingInfo*](aws-properties-ssm-maintenancewindowtask-logginginfo.md)
  }
}
```

### YAML<a name="aws-resource-ssm-maintenancewindowtask-syntax.yaml"></a>

```
Type: "AWS::SSM::MaintenanceWindowTask"
Properties:
  [MaxErrors](#cfn-ssm-maintenancewindowtask-maxerrors): String
  [Description](#cfn-ssm-maintenancewindowtask-description): String
  [ServiceRoleArn](#cfn-ssm-maintenancewindowtask-servicerolearn): String
  [Priority](#cfn-ssm-maintenancewindowtask-priority): Integer
  [MaxConcurrency](#cfn-ssm-maintenancewindowtask-maxconcurrency): String
  [Targets](#cfn-ssm-maintenancewindowtask-targets): 
    - [*Target*](aws-properties-ssm-maintenancewindowtask-target.md)
  [Name](#cfn-ssm-maintenancewindowtask-name): String
  [TaskArn](#cfn-ssm-maintenancewindowtask-taskarn): String
  [TaskInvocationParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters):
    [*TaskInvocationParameters*](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md)
  [WindowId](#cfn-ssm-maintenancewindowtask-windowid): String
  [TaskParameters](#cfn-ssm-maintenancewindowtask-taskparameters):
    JSON object
  [TaskType](#cfn-ssm-maintenancewindowtask-tasktype): String
  [LoggingInfo](#cfn-ssm-maintenancewindowtask-logginginfo): 
    [*LoggingInfo*](aws-properties-ssm-maintenancewindowtask-logginginfo.md)
```

## Properties<a name="aws-resource-ssm-maintenancewindowtask-properties"></a>

`MaxErrors`  <a name="cfn-ssm-maintenancewindowtask-maxerrors"></a>
The maximum number of errors allowed before this task stops being scheduled\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-ssm-maintenancewindowtask-description"></a>
A description of the task\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ServiceRoleArn`  <a name="cfn-ssm-maintenancewindowtask-servicerolearn"></a>
The role that's used when the task is executed\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Priority`  <a name="cfn-ssm-maintenancewindowtask-priority"></a>
The priority of the task in the Maintenance Window\. The lower the number, the higher the priority\. Tasks that have the same priority are scheduled in parallel\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxConcurrency`  <a name="cfn-ssm-maintenancewindowtask-maxconcurrency"></a>
The maximum number of targets that you can run this task for, in parallel\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Targets`  <a name="cfn-ssm-maintenancewindowtask-targets"></a>
The targets, either instances or tags\.  
+ Specify instances using `Key=instanceids,Values=instanceid1,instanceid2`\.
+ Specify tags using `Key=tag name,Values=tag value`\.
 *Required*: Yes  
 *Type*: List of [Systems Manager MaintenanceWindowTask Target](aws-properties-ssm-maintenancewindowtask-target.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-ssm-maintenancewindowtask-name"></a>
The task name\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TaskArn`  <a name="cfn-ssm-maintenancewindowtask-taskarn"></a>
The resource that the task uses during execution\.  
For `RUN_COMMAND` and `AUTOMATION` task types, `TaskArn` is the SSM document name or Amazon Resource Name \(ARN\)\.  
For `LAMBDA` tasks, `TaskArn` is the function name or ARN\.  
For `STEP_FUNCTION` tasks, `TaskArn` is the state machine ARN\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TaskInvocationParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters"></a>
The parameters for task execution\.  
 *Required*: No  
 *Type*: [Systems Manager MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`WindowId`  <a name="cfn-ssm-maintenancewindowtask-windowid"></a>
The ID of the Maintenance Window where the task is registered\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`TaskParameters`  <a name="cfn-ssm-maintenancewindowtask-taskparameters"></a>
The parameters to pass to the task when it's executed\.  
`TaskParameters` has been deprecated\. To specify parameters to pass to a task when it runs, instead use the `Parameters` option in the `TaskInvocationParameters` structure\. For information about how Systems Manager handles these options for the supported Maintenance Window task types, see [AWS Systems Manager MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md)\.
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TaskType`  <a name="cfn-ssm-maintenancewindowtask-tasktype"></a>
The type of task\. Valid values: `RUN_COMMAND`, `AUTOMATION`, `LAMBDA`, `STEP_FUNCTION`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LoggingInfo`  <a name="cfn-ssm-maintenancewindowtask-logginginfo"></a>
Information about an Amazon S3 bucket to write task\-level logs to\.  
`LoggingInfo` has been deprecated\. To specify an S3 bucket to contain logs, instead use the `OutputS3BucketName` and `OutputS3KeyPrefix` options in the `TaskInvocationParameters` structure\. For information about how Systems Manager handles these options for the supported Maintenance Window task types, see [AWS Systems Manager MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md)\.
 *Required*: No  
 *Type*: [Systems Manager MaintenanceWindowTask LoggingInfo](aws-properties-ssm-maintenancewindowtask-logginginfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-ssm-maintenancewindowtask-returnvalues"></a>

### Ref<a name="w3ab2c21c10e1162b9b3"></a>

When you pass the logical ID of an `AWS::SSM::MaintenanceWindowTask` resource to the intrinsic `Ref` function, the function returns the physical ID of the resource, such as `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## See Also<a name="aws-resource-ssm-maintenancewindowtask-seealso"></a>
+ [AWS::SSM::MaintenanceWindow](aws-resource-ssm-maintenancewindow.md)
+ [AWS::SSM::MaintenanceWindowTarget](aws-resource-ssm-maintenancewindowtarget.md)
+ [ RegisterTaskWithMaintenanceWindow](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*