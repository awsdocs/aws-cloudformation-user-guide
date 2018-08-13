# AWS Systems Manager MaintenanceWindowTask MaintenanceWindowStepFunctionsParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-description"></a>The `MaintenanceWindowStepFunctionsParameters` property type specifies the parameters for execution of the `STEP_FUNCTION` for a Maintenance Window task in AWS Systems Manager\.

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-inheritance"></a> `MaintenanceWindowStepFunctionsParameters` is a property of the [Systems Manager MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-syntax.json"></a>

```
{
  "[Input](#cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-input)" : String,
  "[Name](#cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-name)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-syntax.yaml"></a>

```
[Input](#cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-input): String
[Name](#cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-name): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-properties"></a>

`Input`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-input"></a>
The inputs for the `STEP_FUNCTION` task\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-name"></a>
The name of the `STEP_FUNCTION` task\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 