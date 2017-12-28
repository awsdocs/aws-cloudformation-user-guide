# Amazon EC2 Systems Manager MaintenanceWindowTask MaintenanceWindowStepFunctionsParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-description"></a>The `MaintenanceWindowStepFunctionsParameters` property type specifies the parameters for execution of the `STEP_FUNCTION` for an Amazon EC2 Systems Manager Maintenance Window task\.

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-inheritance"></a> `MaintenanceWindowStepFunctionsParameters` is a property of the [SSM MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-input)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-name)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-input): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-name): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-properties"></a>

`Input`  
The inputs for the `STEP_FUNCTION` task\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Name`  
The name of the `STEP_FUNCTION` task\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 