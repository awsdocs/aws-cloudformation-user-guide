# AWS Systems Manager MaintenanceWindowTask TaskInvocationParameters<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-description"></a>The `TaskInvocationParameters` property type specifies the task execution parameters for a Maintenance Window task in AWS Systems Manager\.

<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-inheritance"></a> `TaskInvocationParameters` is a property of the [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md) resource\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax.json"></a>

```
{
  "[MaintenanceWindowRunCommandParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowruncommandparameters)" : [*MaintenanceWindowRunCommandParameters*](aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters.md),
  "[MaintenanceWindowAutomationParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowautomationparameters)" : [*MaintenanceWindowAutomationParameters*](aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters.md),
  "[MaintenanceWindowStepFunctionsParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowstepfunctionsparameters)" : [*MaintenanceWindowStepFunctionsParameters*](aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters.md),
  "[MaintenanceWindowLambdaParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowlambdaparameters)" : [*MaintenanceWindowLambdaParameters*](aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters.md)
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax.yaml"></a>

```
[MaintenanceWindowRunCommandParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowruncommandparameters):
  [*MaintenanceWindowRunCommandParameters*](aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters.md)
[MaintenanceWindowAutomationParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowautomationparameters):
  [*MaintenanceWindowAutomationParameters*](aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters.md)
[MaintenanceWindowStepFunctionsParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowstepfunctionsparameters):
  [*MaintenanceWindowStepFunctionsParameters*](aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters.md)
[MaintenanceWindowLambdaParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowlambdaparameters):
  [*MaintenanceWindowLambdaParameters*](aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters.md)
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-properties"></a>

`MaintenanceWindowRunCommandParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowruncommandparameters"></a>
The parameters for a `RUN_COMMAND` task type\.  
 *Required*: No  
 *Type*: [Systems Manager MaintenanceWindowTask MaintenanceWindowRunCommandParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaintenanceWindowAutomationParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowautomationparameters"></a>
The parameters for an `AUTOMATION` task type\.  
 *Required*: No  
 *Type*: [Systems Manager MaintenanceWindowTask MaintenanceWindowAutomationParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaintenanceWindowStepFunctionsParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowstepfunctionsparameters"></a>
The parameters for a `STEP_FUNCTION` task type\.  
 *Required*: No  
 *Type*: [Systems Manager MaintenanceWindowTask MaintenanceWindowStepFunctionsParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaintenanceWindowLambdaParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowlambdaparameters"></a>
The parameters for a `LAMBDA` task type\.  
 *Required*: No  
 *Type*: [Systems Manager MaintenanceWindowTask MaintenanceWindowLambdaParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 