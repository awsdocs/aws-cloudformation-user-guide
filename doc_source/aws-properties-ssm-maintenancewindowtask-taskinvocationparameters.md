# Amazon EC2 Systems Manager MaintenanceWindowTask TaskInvocationParameters<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-description"></a>The `TaskInvocationParameters` property type specifies the parameters for task execution for an Amazon EC2 Systems Manager Maintenance Window task\.

<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-inheritance"></a> `TaskInvocationParameters` is a property of the [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md) resource\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowruncommandparameters)" : MaintenanceWindowRunCommandParameters,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowautomationparameters)" : MaintenanceWindowAutomationParameters,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowstepfunctionsparameters)" : MaintenanceWindowStepFunctionsParameters,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowlambdaparameters)" : MaintenanceWindowLambdaParameters
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowruncommandparameters):
  MaintenanceWindowRunCommandParameters
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowautomationparameters):
  MaintenanceWindowAutomationParameters
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowstepfunctionsparameters):
  MaintenanceWindowStepFunctionsParameters
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowlambdaparameters):
  MaintenanceWindowLambdaParameters
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-properties"></a>

`MaintenanceWindowRunCommandParameters`  
The parameters for a `RUN_COMMAND` task type\.  
 *Required*: No  
 *Type*: [SSM MaintenanceWindowTask MaintenanceWindowRunCommandParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters.md)  
 *Update requires*: No interruption 

`MaintenanceWindowAutomationParameters`  
The parameters for an `AUTOMATION` task type\.  
 *Required*: No  
 *Type*: [SSM MaintenanceWindowTask MaintenanceWindowAutomationParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters.md)  
 *Update requires*: No interruption 

`MaintenanceWindowStepFunctionsParameters`  
The parameters for a `STEP_FUNCTION` task type\.  
 *Required*: No  
 *Type*: [SSM MaintenanceWindowTask MaintenanceWindowStepFunctionsParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters.md)  
 *Update requires*: No interruption 

`MaintenanceWindowLambdaParameters`  
The parameters for a `LAMBDA` task type\.  
 *Required*: No  
 *Type*: [SSM MaintenanceWindowTask MaintenanceWindowLambdaParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters.md)  
 *Update requires*: No interruption 