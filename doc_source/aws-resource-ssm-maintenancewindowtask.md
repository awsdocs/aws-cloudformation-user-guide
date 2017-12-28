# AWS::SSM::MaintenanceWindowTask<a name="aws-resource-ssm-maintenancewindowtask"></a>

The `AWS::SSM::MaintenanceWindowTask` resource defines information about a task for a Maintenance Window for Amazon EC2 Systems Manager\. For more information, see [ RegisterTaskWithMaintenanceWindow](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *Amazon EC2 Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindowtask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindowtask-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindowTask",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maxerrors)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-servicerolearn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-priority)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maxconcurrency)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-targets)" : [ Target, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskarn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters)" : TaskInvocationParameters,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-windowid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskparameters)" : JSON object,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-tasktype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-logginginfo)" : LoggingInfo
  }
}
```

### YAML<a name="aws-resource-ssm-maintenancewindowtask-syntax.yaml"></a>

```
Type: "AWS::SSM::MaintenanceWindowTask"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maxerrors): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-servicerolearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-priority): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maxconcurrency): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-targets): 
    - Target
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters):
    TaskInvocationParameters
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-windowid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskparameters):
    JSON object
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-tasktype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-logginginfo): 
    LoggingInfo
```

## Properties<a name="aws-resource-ssm-maintenancewindowtask-properties"></a>

`MaxErrors`  
The maximum number of errors allowed before this task stops being scheduled\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Description`  
A description of the task\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ServiceRoleArn`  
The role that's used when the task is executed\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Priority`  
The priority of the task in the Maintenance Window\. The lower the number, the higher the priority\. Tasks that have the same priority are scheduled in parallel\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: No interruption 

`MaxConcurrency`  
The maximum number of targets that you can run this task for, in parallel\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Targets`  
The targets, either instances or tags\.  

+ Specify instances using `Key=instanceids,Values=instanceid1,instanceid2`\.

+ Specify tags using `Key=tag name,Values=tag value`\.
 *Required*: Yes  
 *Type*: List of [SSM MaintenanceWindowTask Target](aws-properties-ssm-maintenancewindowtask-target.md)  
 *Update requires*: No interruption 

`Name`  
The task name\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`TaskArn`  
The resource that the task uses during execution\.  
For `RUN_COMMAND` and `AUTOMATION` task types, `TaskArn` is the SSM document name or Amazon Resource Name \(ARN\)\.  
For `LAMBDA` tasks, `TaskArn` is the function name or ARN\.  
For `STEP_FUNCTION` tasks, `TaskArn` is the state machine ARN\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`TaskInvocationParameters`  
The parameters for task execution\.  
 *Required*: No  
 *Type*: [SSM MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md)  
 *Update requires*: No interruption 

`WindowId`  
The ID of the Maintenance Window where the task is registered\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`TaskParameters`  
The parameters to pass to the task when it's executed\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: No interruption 

`TaskType`  
The type of task\. Valid values: `RUN_COMMAND`, `AUTOMATION`, `LAMBDA`, `STEP_FUNCTION`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`LoggingInfo`  
Information about an Amazon S3 bucket to write task\-level logs to\.  
 *Required*: No  
 *Type*: [SSM MaintenanceWindowTask LoggingInfo](aws-properties-ssm-maintenancewindowtask-logginginfo.md)  
 *Update requires*: No interruption 

## Return Values<a name="aws-resource-ssm-maintenancewindowtask-returnvalues"></a>

### Ref<a name="w3ab2c21c10e1018b9b3"></a>

When you pass the logical ID of an `AWS::SSM::MaintenanceWindowTask` resource to the intrinsic `Ref` function, the function returns the physical ID of the resource, such as `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`\. 

For more information about using the `Ref` function, see Ref\. 

## See Also<a name="aws-resource-ssm-maintenancewindowtask-seealso"></a>

+ [AWS::SSM::MaintenanceWindow](aws-resource-ssm-maintenancewindow.md)

+ [AWS::SSM::MaintenanceWindowTarget](aws-resource-ssm-maintenancewindowtarget.md)

+ [ RegisterTaskWithMaintenanceWindow](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *Amazon EC2 Systems Manager API Reference*