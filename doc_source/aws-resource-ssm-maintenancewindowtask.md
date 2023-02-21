# AWS::SSM::MaintenanceWindowTask<a name="aws-resource-ssm-maintenancewindowtask"></a>

The `AWS::SSM::MaintenanceWindowTask` resource defines information about a task for an AWS Systems Manager maintenance window\. For more information, see [RegisterTaskWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindowtask-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindowtask-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindowTask",
  "Properties" : {
      "[CutoffBehavior](#cfn-ssm-maintenancewindowtask-cutoffbehavior)" : String,
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
  [CutoffBehavior](#cfn-ssm-maintenancewindowtask-cutoffbehavior): String
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

`CutoffBehavior`  <a name="cfn-ssm-maintenancewindowtask-cutoffbehavior"></a>
The specification for whether tasks should continue to run after the cutoff time specified in the maintenance windows is reached\.   
*Required*: No  
*Type*: String  
*Allowed values*: `CANCEL_TASK | CONTINUE_TASK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ssm-maintenancewindowtask-description"></a>
A description of the task\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingInfo`  <a name="cfn-ssm-maintenancewindowtask-logginginfo"></a>
Information about an Amazon S3 bucket to write Run Command task\-level logs to\.  
 `LoggingInfo` has been deprecated\. To specify an Amazon S3 bucket to contain logs for Run Command tasks, instead use the `OutputS3BucketName` and `OutputS3KeyPrefix` options in the `TaskInvocationParameters` structure\. For information about how Systems Manager handles these options for the supported maintenance window task types, see [AWS::SSM::MaintenanceWindowTask MaintenanceWindowRunCommandParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters.html)\.
*Required*: No  
*Type*: [LoggingInfo](aws-properties-ssm-maintenancewindowtask-logginginfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxConcurrency`  <a name="cfn-ssm-maintenancewindowtask-maxconcurrency"></a>
The maximum number of targets this task can be run for, in parallel\.  
Although this element is listed as "Required: No", a value can be omitted only when you are registering or updating a [targetless task](https://docs.aws.amazon.com/systems-manager/latest/userguide/maintenance-windows-targetless-tasks.html) You must provide a value in all other cases\.  
For maintenance window tasks without a target specified, you can't supply a value for this option\. Instead, the system inserts a placeholder value of `1`\. This value doesn't affect the running of your task\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `7`  
*Pattern*: `^([1-9][0-9]*|[1-9][0-9]%|[1-9]%|100%)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxErrors`  <a name="cfn-ssm-maintenancewindowtask-maxerrors"></a>
The maximum number of errors allowed before this task stops being scheduled\.  
Although this element is listed as "Required: No", a value can be omitted only when you are registering or updating a [targetless task](https://docs.aws.amazon.com/systems-manager/latest/userguide/maintenance-windows-targetless-tasks.html) You must provide a value in all other cases\.  
For maintenance window tasks without a target specified, you can't supply a value for this option\. Instead, the system inserts a placeholder value of `1`\. This value doesn't affect the running of your task\.
*Required*: No  
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
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) service role to use to publish Amazon Simple Notification Service \(Amazon SNS\) notifications for maintenance window Run Command tasks\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-ssm-maintenancewindowtask-targets"></a>
The targets, either instances or window target IDs\.  
+ Specify instances using `Key=InstanceIds,Values=instanceid1,instanceid2 `\.
+ Specify window target IDs using `Key=WindowTargetIds,Values=window-target-id-1,window-target-id-2`\.
*Required*: No  
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
                    }
                },
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
      TaskInvocationParameters:
        MaintenanceWindowRunCommandParameters:
          Parameters:
            Operation:
            - Install
            RebootOption:
            - NoReboot
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
        - TestResourceGroup
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
    Type: AWS::SSM::MaintenanceWindowTask
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
          Parameters:
            Operation:
            - Install
            RebootOption:
            - NoReboot
      MaxConcurrency: 7
      MaxErrors: 7
      Priority: 5
      DependsOn: MaintenanceWindowTarget
```

### Create a Run Command task that runs a PowerShell script<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_runs_a_PowerShell_script"></a>

The following example demonstrates running a command with AWS\-RunPowerShellScript\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_runs_a_PowerShell_script--json"></a>

```
{
    "Resources": {
        "MaintenanceWindowRunCommandTask": {
            "Type": "AWS::SSM::MaintenanceWindowTask",
            "Properties": {
                "WindowId": {
                    "Ref": "MaintenanceWindow"
                },
                "Targets": [
                    {
                        "Key": "WindowTargetIds",
                        "Values": [
                            "MaintenanceWindowTarget"
                        ]
                    }
                ],
                "TaskType": "RUN_COMMAND",
                "TaskArn": "AWS-RunPowerShellScript",
                "TaskInvocationParameters": {
                    "MaintenanceWindowRunCommandParameters": {
                        "Comment": "This is a comment",
                        "CloudWatchOutputConfig": {
                            "CloudWatchLogGroupName": "MyLogGroupName",
                            "CloudWatchOutputEnabled": true
                        },
                        "Parameters": {
                            "executionTimeout": [
                                "3600"
                            ],
                            "commands": [
                                "Get-Service myImportantService | Restart-Service\nGet-ExecutionPolicy -List\nSet-ExecutionPolicy -Scope Process AllSigned\n"
                            ]
                        }
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
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_Run_Command_task_that_runs_a_PowerShell_script--yaml"></a>

```
---
Resources:
  MaintenanceWindowRunCommandTask:
    Type: 'AWS::SSM::MaintenanceWindowTask'
    Properties:
      WindowId: !Ref MaintenanceWindow
      Targets:
        - Key: WindowTargetIds
          Values:
            - MaintenanceWindowTarget
      TaskType: RUN_COMMAND
      TaskArn: AWS-RunPowerShellScript
      TaskInvocationParameters:
        MaintenanceWindowRunCommandParameters:
          Comment: This is a comment
          CloudWatchOutputConfig:
            CloudWatchLogGroupName: MyLogGroupName
            CloudWatchOutputEnabled: true
          Parameters:
            executionTimeout:
              - '3600'
            commands:
              - Get-Service myImportantService | Restart-Service
              - Get-ExecutionPolicy -List
              - Set-ExecutionPolicy -Scope Process AllSigned
      MaxConcurrency: 7
      MaxErrors: 7
      Priority: 5
    DependsOn: MaintenanceWindowTarget
```

### Create a task that runs an Automation runbook<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_task_that_runs_an_Automation_runbook"></a>

The following example creates a Systems Manager maintenance window task that uses the runbook `AWS-PatchInstanceWithRollback` to patch instances\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_task_that_runs_an_Automation_runbook--json"></a>

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
                "TaskArn": "AWS-PatchInstanceWithRollback",
                "ServiceRoleArn": "AutomationRole.Arn",
                "TaskType": "AUTOMATION",
                "TaskInvocationParameters": {
                    "MaintenanceWindowAutomationParameters": {
                        "DocumentVersion": "1",
                        "Parameters": {
                            "instanceId": [
                                "{{RESOURCE_ID}}"
                            ]
                        }
                    }
                },
                "Priority": 1,
                "MaxConcurrency": 5,
                "MaxErrors": 5,
                "Name": "AutomationTask"
            },
            "DependsOn": "MaintenanceWindowTarget"
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_task_that_runs_an_Automation_runbook--yaml"></a>

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
      TaskArn: AWS-PatchInstanceWithRollback
      ServiceRoleArn: AutomationRole.Arn
      TaskType: AUTOMATION
      TaskInvocationParameters:
        MaintenanceWindowAutomationParameters:
          DocumentVersion: 1
          Parameters:
            instanceId:
              - '{{RESOURCE_ID}}'
      Priority: 1
      MaxConcurrency: 5
      MaxErrors: 5
      Name: AutomationTask
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
    Type: 'AWS::SSM::MaintenanceWindowTask'
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

### Create a task that runs an AWS Lambda function<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_task_that_runs_an__function"></a>

The following example runs an AWS Lambda function to restart instances\.

**Note**  
The value for `Payload` in `MaintenanceWindowLambdaParameters` must be formatted as a Base64\-encoded binary data object\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_task_that_runs_an__function--json"></a>

```
{
   "Resources": {
      "LambdaTask": {
         "Type": "AWS::SSM::MaintenanceWindowTask",
         "Properties": {
            "WindowId": "mw-04fd6f19dfEXAMPLE",
            "TaskArn": "arn:aws:lambda:us-east-2:111222333444:function:MyLambdaTaskArn",
            "ServiceRoleArn": "arn:aws:iam::111222333444:role/aws-service-role/ssm.amazonaws.com/AWSServiceRoleForAmazonSSM",
            "TaskType": "LAMBDA",
            "TaskInvocationParameters": {
               "MaintenanceWindowLambdaParameters": {
                  "ClientContext": "eyJ0ZXN0Q29udGV4dCI6Ik5vdGhp==trucated==EXAMPLE",
                  "Qualifier": "$LATEST",
                  "Payload": "eyJJbnN0YW5jZUlkIjoie3tSRVNPVVJDRV9JRH19IiwidGFyZ2V0VHlwZSI6Int7VEFSR0VUX1RZUEV9fSJ9"
               }
            },
            "Priority": 1,
            "Name": "UpdateLambdaTaskEXAMPLE"
         }
      }
   }
}
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtask--examples--Create_a_task_that_runs_an__function--yaml"></a>

```
---
Resources:
  LambdaTask:
    Type: 'AWS::SSM::MaintenanceWindowTask'
    Properties:
      WindowId: mw-04fd6f19dfEXAMPLE
      TaskArn: >-
        arn:aws:lambda:us-east-2:111222333444:function:MyLambdaTaskArn
      ServiceRoleArn: >-
        arn:aws:iam::111222333444:role/aws-service-role/ssm.amazonaws.com/AWSServiceRoleForAmazonSSM
      TaskType: LAMBDA
      TaskInvocationParameters:
        MaintenanceWindowLambdaParameters:
          ClientContext: eyJ0ZXN0Q29udGV4dCI6Ik5vdGhp==trucated==EXAMPLE
          Qualifier: $LATEST
          Payload: >-
            eyJJbnN0YW5jZUlkIjoie3tSRVNPVVJDRV9JRH19IiwidGFyZ2V0VHlwZSI6Int7VEFSR0VUX1RZUEV9fSJ9
      Priority: 1
      Name: UpdateLambdaTaskEXAMPLE
```

## See also<a name="aws-resource-ssm-maintenancewindowtask--seealso"></a>
+  [AWS::SSM::MaintenanceWindow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindow.html) 
+  [AWS::SSM::MaintenanceWindowTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtarget.html) 
+  [RegisterTaskWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.