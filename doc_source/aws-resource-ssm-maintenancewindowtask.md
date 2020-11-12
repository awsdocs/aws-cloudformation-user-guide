# AWS::SSM::MaintenanceWindowTask<a name="aws-resource-ssm-maintenancewindowtask"></a>

The `AWS::SSM::MaintenanceWindowTask` resource defines information about a task for an AWS Systems Manager maintenance window\. For more information, see [RegisterTaskWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindowtask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindowtask-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindowTask",
  "Properties" : {
      "[Description](#cfn-ssm-maintenancewindowtask-description)" : String,
      "[LoggingInfo](#cfn-ssm-maintenancewindowtask-logginginfo)" : LoggingInfo,
      "[MaxConcurrency](#cfn-ssm-maintenancewindowtask-maxconcurrency)" : String,
      "[MaxErrors](#cfn-ssm-maintenancewindowtask-maxerrors)" : String,
      "[Name](#cfn-ssm-maintenancewindowtask-name)" : String,
      "[Priority](#cfn-ssm-maintenancewindowtask-priority)" : Integer,
      "[ServiceRoleArn](#cfn-ssm-maintenancewindowtask-servicerolearn)" : String,
      "[Targets](#cfn-ssm-maintenancewindowtask-targets)" : [ Target, ... ],
      "[TaskArn](#cfn-ssm-maintenancewindowtask-taskarn)" : String,
      "[TaskInvocationParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters)" : TaskInvocationParameters,
      "[TaskParameters](#cfn-ssm-maintenancewindowtask-taskparameters)" : Json,
      "[TaskType](#cfn-ssm-maintenancewindowtask-tasktype)" : String,
      "[WindowId](#cfn-ssm-maintenancewindowtask-windowid)" : String
    }
}
```

### YAML<a name="aws-resource-ssm-maintenancewindowtask-syntax.yaml"></a>

```
Type: AWS::SSM::MaintenanceWindowTask
Properties: 
  [Description](#cfn-ssm-maintenancewindowtask-description): String
  [LoggingInfo](#cfn-ssm-maintenancewindowtask-logginginfo): 
    LoggingInfo
  [MaxConcurrency](#cfn-ssm-maintenancewindowtask-maxconcurrency): String
  [MaxErrors](#cfn-ssm-maintenancewindowtask-maxerrors): String
  [Name](#cfn-ssm-maintenancewindowtask-name): String
  [Priority](#cfn-ssm-maintenancewindowtask-priority): Integer
  [ServiceRoleArn](#cfn-ssm-maintenancewindowtask-servicerolearn): String
  [Targets](#cfn-ssm-maintenancewindowtask-targets): 
    - Target
  [TaskArn](#cfn-ssm-maintenancewindowtask-taskarn): String
  [TaskInvocationParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters): 
    TaskInvocationParameters
  [TaskParameters](#cfn-ssm-maintenancewindowtask-taskparameters): Json
  [TaskType](#cfn-ssm-maintenancewindowtask-tasktype): String
  [WindowId](#cfn-ssm-maintenancewindowtask-windowid): String
```

## Properties<a name="aws-resource-ssm-maintenancewindowtask-properties"></a>

`Description`  <a name="cfn-ssm-maintenancewindowtask-description"></a>
A description of the task\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingInfo`  <a name="cfn-ssm-maintenancewindowtask-logginginfo"></a>
Information about an Amazon S3 bucket to write task\-level logs to\.  
 `LoggingInfo` has been deprecated\. To specify an S3 bucket to contain logs, instead use the `OutputS3BucketName` and `OutputS3KeyPrefix` options in the `TaskInvocationParameters` structure\. For information about how Systems Manager handles these options for the supported maintenance window task types, see [AWS Systems Manager MaintenanceWindowTask TaskInvocationParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.html)\.
*Required*: No  
*Type*: [LoggingInfo](aws-properties-ssm-maintenancewindowtask-logginginfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxConcurrency`  <a name="cfn-ssm-maintenancewindowtask-maxconcurrency"></a>
The maximum number of targets this task can be run for, in parallel\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `7`  
*Pattern*: `^([1-9][0-9]*|[1-9][0-9]%|[1-9]%|100%)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxErrors`  <a name="cfn-ssm-maintenancewindowtask-maxerrors"></a>
The maximum number of errors allowed before this task stops being scheduled\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `7`  
*Pattern*: `^([1-9][0-9]*|[0]|[1-9][0-9]%|[0-9]%|100%)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssm-maintenancewindowtask-name"></a>
The task name\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-ssm-maintenancewindowtask-priority"></a>
The priority of the task in the maintenance window\. The lower the number, the higher the priority\. Tasks that have the same priority are scheduled in parallel\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRoleArn`  <a name="cfn-ssm-maintenancewindowtask-servicerolearn"></a>
The ARN of the IAM service role to use to publish Amazon Simple Notification Service \(Amazon SNS\) notifications for maintenance window Run Command tasks\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-ssm-maintenancewindowtask-targets"></a>
The targets, either instances or window target IDs\.  
+ Specify instances using `Key=InstanceIds,Values=instanceid1,instanceid2 `\.
+ Specify window target IDs using `Key=WindowTargetIds,Values=window-target-id-1,window-target-id-2`\.
*Required*: Yes  
*Type*: List of [Target](aws-properties-ssm-maintenancewindowtask-target.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskArn`  <a name="cfn-ssm-maintenancewindowtask-taskarn"></a>
The resource that the task uses during execution\.  
For `RUN_COMMAND` and `AUTOMATION` task types, `TaskArn` is the SSM document name or Amazon Resource Name \(ARN\)\.  
For `LAMBDA` tasks, `TaskArn` is the function name or ARN\.  
For `STEP_FUNCTIONS` tasks, `TaskArn` is the state machine ARN\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskInvocationParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters"></a>
The parameters to pass to the task when it runs\. Populate only the fields that match the task type\. All other fields should be empty\.   
When you update a maintenance window task that has options specified in `TaskInvocationParameters`, you must provide again all the `TaskInvocationParameters` values that you want to retain\. The values you do not specify again are removed\. For example, suppose that when you registered a Run Command task, you specified `TaskInvocationParameters` values for `Comment`, `NotificationConfig`, and `OutputS3BucketName`\. If you update the maintenance window task and specify only a different `OutputS3BucketName` value, the values for `Comment` and `NotificationConfig` are removed\.
*Required*: No  
*Type*: [TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskParameters`  <a name="cfn-ssm-maintenancewindowtask-taskparameters"></a>
The parameters to pass to the task when it runs\.  
 `TaskParameters` has been deprecated\. To specify parameters to pass to a task when it runs, instead use the `Parameters` option in the `TaskInvocationParameters` structure\. For information about how Systems Manager handles these options for the supported maintenance window task types, see [MaintenanceWindowTaskInvocationParameters](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_MaintenanceWindowTaskInvocationParameters.html)\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskType`  <a name="cfn-ssm-maintenancewindowtask-tasktype"></a>
The type of task\. Valid values: `RUN_COMMAND`, `AUTOMATION`, `LAMBDA`, `STEP_FUNCTIONS`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AUTOMATION | LAMBDA | RUN_COMMAND | STEP_FUNCTIONS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WindowId`  <a name="cfn-ssm-maintenancewindowtask-windowid"></a>
The ID of the maintenance window where the task is registered\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `20`  
*Pattern*: `^mw-[0-9a-f]{17}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ssm-maintenancewindowtask-return-values"></a>

### Ref<a name="aws-resource-ssm-maintenancewindowtask-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the maintenance window task ID, such as `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ssm-maintenancewindowtask--examples"></a>

### Create a Run Command task that targets instances using a resource group name<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_targets_instances_using_a_resource_group_name"></a>

The following example creates a maintenance window Run Command task that installs patches on instances using a using a resource group name as the target\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_targets_instances_using_a_resource_group_name--json"></a>

```
{
    "Resources": {
        "PatchTask": {
            "Type": "AWS::SSM::MaintenanceWindowTask",
            "Properties": {
                "Description": "Apply OS patches on instances in target",
                "MaxConcurrency": 1,
                "MaxErrors": 1,
                "Priority": 0,
                "TaskType": "RUN_COMMAND",
                "WindowId": {
                    "Ref": "MaintenanceWindow"
                },
                "TaskArn": "AWS-RunPatchBaseline",
                "Targets": [
                    {
                        "Key": "WindowTargetIds",
                        "Values": [
                            {
                                "Ref": "MaintenanceWindowTarget"
                            }
                        ]
                    }
                ]
            }
        },
        "MaintenanceWindow": {
            "Type": "AWS::SSM::MaintenanceWindow",
            "Properties": {
                "Name": "MaintenanceWindow",
                "AllowUnassociatedTargets": true,
                "Cutoff": 0,
                "Description": "Maintenance window for instances",
                "Duration": 1,
                "Schedule": "cron(20 17 ? * MON-FRI *)"
            }
        },
        "MaintenanceWindowTarget": {
            "Type": "AWS::SSM::MaintenanceWindowTarget",
            "Properties": {
                "ResourceType": "RESOURCE_GROUP",
                "Targets": [
                    {
                        "Key": "resource-groups:Name",
                        "Values": [
                            "TestResourceGroup"
                        ]
                    }
                ],
                "WindowId": {
                    "Ref": "MaintenanceWindow"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_targets_instances_using_a_resource_group_name--yaml"></a>

```
---
Resources:
  PatchTask:
    Type: AWS::SSM::MaintenanceWindowTask
    Properties:
      Description: Apply OS patches on instances in target
      MaxConcurrency: 1
      MaxErrors: 1
      Priority: 0
      TaskType: RUN_COMMAND
      WindowId:
        Ref: MaintenanceWindow
      TaskArn: AWS-RunPatchBaseline
      Targets:
        - Key: WindowTargetIds
          Values:
            - Ref: MaintenanceWindowTarget

  MaintenanceWindow:
    Type: AWS::SSM::MaintenanceWindow
    Properties:
      Name: MaintenanceWindow
      AllowUnassociatedTargets: true
      Cutoff: 0
      Description: Maintenance window for instances
      Duration: 1
      Schedule: cron(20 17 ? * MON-FRI *)

  MaintenanceWindowTarget:
    Type: AWS::SSM::MaintenanceWindowTarget
    Properties: 
      ResourceType: RESOURCE_GROUP
      Targets:
        - Key: resource-groups:Name
          Values:
            - "TestResourceGroup"
      WindowId: 
        Ref: MaintenanceWindow
```

### Create a Run Command task that targets instances using a maintenance window target ID<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_targets_instances_using_a_maintenance_window_target_ID"></a>

The following example creates a maintenance window Run Command task that installs patches on instances but does not reboot them\. The maintenance window task targets managed instances using a maintenance window target ID\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_targets_instances_using_a_maintenance_window_target_ID--json"></a>

```
{
    "Resources": {
        "MaintenanceWindowRunCommandTask": {
            "Type": "AWS::SSM::MaintenanceWindowTask",
            "Properties": {
                "WindowId": "MaintenanceWindow",
                "Targets": [
                    {
                        "Key": "WindowTargetIds",
                        "Values": [
                            "MaintenanceWindowTarget"
                        ]
                    }
                ],
                "TaskType": "RUN_COMMAND",
                "TaskArn": "AWS-RunPatchBaseline",
                "TaskInvocationParameters": {
                    "MaintenanceWindowRunCommandParameters": {
                        "Parameters": {
                            "Operation": [
                                "Install"
                            ],
                            "RebootOption": [
                                "NoReboot"
                            ]
                        }
                    },
                    "MaxConcurrency": 7,
                    "MaxErrors": 7,
                    "Priority": 5
                },
                "DependsOn": "MaintenanceWindowTarget"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_targets_instances_using_a_maintenance_window_target_ID--yaml"></a>

```
---
Resources:
  MaintenanceWindowRunCommandTask:
    Type: 'AWS::SSM::MaintenanceWindowTask'
    Properties:
      WindowId: MaintenanceWindow
      Targets:
        - Key: WindowTargetIds
          Values:
            - MaintenanceWindowTarget
      TaskType: RUN_COMMAND
      TaskArn: AWS-RunPatchBaseline
      TaskInvocationParameters:
        MaintenanceWindowRunCommandParameters:
          Comment: Running security updates for OS with no reboot
          Parameters:
            Operation:
              - Install
            RebootOption:
              - NoReboot
      MaxConcurrency: 7
      MaxErrors: 100%
      Priority: 5
    DependsOn: MaintenanceWindowTarget
```

### Create a Step Functions task that targets a maintenance window target ID<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Step_Functions_task_that_targets_a_maintenance_window_target_ID"></a>

The following example creates a Systems Manager maintenance window task that runs the specified Step Function\. The maintenance window task targets managed instances using a maintenance window target ID\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Step_Functions_task_that_targets_a_maintenance_window_target_ID--json"></a>

```
{
    "Resources": {
        "MaintenanceWindowStepFunctionsTask": {
            "Type": "AWS::SSM::MaintenanceWindowTask",
            "Properties": {
                "WindowId": "MaintenanceWindow",
                "Targets": [
                    {
                        "Key": "WindowTargetIds",
                        "Values": [
                            "MaintenanceWindowTarget"
                        ]
                    }
                ],
                "TaskArn": "SSMStepFunctionDemo",
                "ServiceRoleArn": "StepFunctionRole.Arn",
                "TaskType": "STEP_FUNCTIONS",
                "TaskInvocationParameters": {
                    "MaintenanceWindowStepFunctionsParameters": {
                        "Input": "{\"instanceId\":\"{{TARGET_ID}}\", \"wait_time\": 20}",
                        "Name": "{{INVOCATION_ID}}"
                    }
                },
                "Priority": 1,
                "MaxConcurrency": 5,
                "MaxErrors": 5,
                "Name": "StepFunctionsTask"
            },
            "DependsOn": "MaintenanceWindowTarget"
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Step_Functions_task_that_targets_a_maintenance_window_target_ID--yaml"></a>

```
---
Resources:
  MaintenanceWindowStepFunctionsTask:
    Type: AWS::SSM::MaintenanceWindowTask
    Properties:
      WindowId: MaintenanceWindow
      Targets:
      - Key: WindowTargetIds
        Values:
        - MaintenanceWindowTarget
      TaskArn: SSMStepFunctionDemo
      ServiceRoleArn: StepFunctionRole.Arn
      TaskType: STEP_FUNCTIONS
      TaskInvocationParameters:
        MaintenanceWindowStepFunctionsParameters:
          Input: '{"instanceId":"{{TARGET_ID}}", "wait_time": 20}'
          Name: "{{INVOCATION_ID}}"
      Priority: 1
      MaxConcurrency: 5
      MaxErrors: 5
      Name: StepFunctionsTask
    DependsOn: MaintenanceWindowTarget
```

### Create a Step Functions task that targets an instance ID<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Step_Functions_task_that_targets_an_instance_ID"></a>

The following example creates a Systems Manager maintenance window task that runs the specified Step Function\. The maintenance window task targets the specified instance IDs\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Step_Functions_task_that_targets_an_instance_ID--json"></a>

```
{
    "Resources": {
        "StepFunctionsTask": {
            "Type": "AWS::SSM::MaintenanceWindowTask",
            "Properties": {
                "WindowId": "MaintenanceWindow",
                "Targets": [
                    {
                        "Key": "InstanceIds",
                        "Values": [
                            "i-012345678912345678"
                        ]
                    }
                ],
                "TaskArn": "SSMStepFunctionDemo",
                "ServiceRoleArn": "StepFunctionRole.Arn",
                "TaskType": "STEP_FUNCTIONS",
                "TaskInvocationParameters": {
                    "MaintenanceWindowStepFunctionsParameters": {
                        "Input": "{\"instanceId\":\"{{TARGET_ID}}\", \"wait_time\": 20}",
                        "Name": "{{INVOCATION_ID}}"
                    }
                },
                "Priority": 1,
                "MaxConcurrency": 5,
                "MaxErrors": 5,
                "Name": "StepFunctionsTask"
            },
            "DependsOn": "MaintenanceWindowTarget"
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Step_Functions_task_that_targets_an_instance_ID--yaml"></a>

```
---
Resources:
  StepFunctionsTask:
    Type: AWS::SSM::MaintenanceWindowTask
    Properties:
      WindowId: MaintenanceWindow
      Targets:
      - Key: InstanceIds
        Values:
        - i-012345678912345678
      TaskArn: SSMStepFunctionDemo
      ServiceRoleArn: StepFunctionRole.Arn
      TaskType: STEP_FUNCTIONS
      TaskInvocationParameters:
        MaintenanceWindowStepFunctionsParameters:
          Input: '{"instanceId":"{{TARGET_ID}}", "wait_time": 20}'
          Name: "{{INVOCATION_ID}}"
      Priority: 1
      MaxConcurrency: 5
      MaxErrors: 5
      Name: StepFunctionsTask
    DependsOn: MaintenanceWindowTarget
```

### Create a maintenance window with run command task\.<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_maintenance_window_with_run_command_task."></a>

The following examples are for the `Parameters` property of the `MaintenanceWindowRunCommandParameters` property type\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_maintenance_window_with_run_command_task.--json"></a>

```
{
    "Parameters": {
        "executionTimeout": [
            "3600"
        ],
        "commands": [
            "Get-Service myImportantService | Restart-Service\nGet-ExecutionPolicy -List\nSet-ExecutionPolicy -Scope Process AllSigned\n"
        ]
    }
}
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_maintenance_window_with_run_command_task.--yaml"></a>

```
Parameters:
  executionTimeout:
    - '3600'
  commands:
    - |
      Get-Service myImportantService | Restart-Service
      Get-ExecutionPolicy -List
      Set-ExecutionPolicy -Scope Process AllSigned
```

## See also<a name="aws-resource-ssm-maintenancewindowtask--seealso"></a>
+  [AWS::SSM::MaintenanceWindow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindow.html) 
+  [AWS::SSM::MaintenanceWindowTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtarget.html) 
+  [RegisterTaskWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.