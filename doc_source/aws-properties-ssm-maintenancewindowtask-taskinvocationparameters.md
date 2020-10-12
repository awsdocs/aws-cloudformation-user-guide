# AWS::SSM::MaintenanceWindowTask TaskInvocationParameters<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters"></a>

The `TaskInvocationParameters` property type specifies the task execution parameters for a maintenance window task in AWS Systems Manager\.

 `TaskInvocationParameters` is a property of the [AWS::SSM::MaintenanceWindowTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtask.html) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax.json"></a>

```
{
  "[MaintenanceWindowAutomationParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowautomationparameters)" : MaintenanceWindowAutomationParameters,
  "[MaintenanceWindowLambdaParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowlambdaparameters)" : MaintenanceWindowLambdaParameters,
  "[MaintenanceWindowRunCommandParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowruncommandparameters)" : MaintenanceWindowRunCommandParameters,
  "[MaintenanceWindowStepFunctionsParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowstepfunctionsparameters)" : MaintenanceWindowStepFunctionsParameters
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-syntax.yaml"></a>

```
  [MaintenanceWindowAutomationParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowautomationparameters): 
    MaintenanceWindowAutomationParameters
  [MaintenanceWindowLambdaParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowlambdaparameters): 
    MaintenanceWindowLambdaParameters
  [MaintenanceWindowRunCommandParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowruncommandparameters): 
    MaintenanceWindowRunCommandParameters
  [MaintenanceWindowStepFunctionsParameters](#cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowstepfunctionsparameters): 
    MaintenanceWindowStepFunctionsParameters
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-taskinvocationparameters-properties"></a>

`MaintenanceWindowAutomationParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowautomationparameters"></a>
The parameters for an `AUTOMATION` task type\.  
*Required*: No  
*Type*: [MaintenanceWindowAutomationParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaintenanceWindowLambdaParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowlambdaparameters"></a>
The parameters for a `LAMBDA` task type\.  
*Required*: No  
*Type*: [MaintenanceWindowLambdaParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaintenanceWindowRunCommandParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowruncommandparameters"></a>
The parameters for a `RUN_COMMAND` task type\.  
*Required*: No  
*Type*: [MaintenanceWindowRunCommandParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaintenanceWindowStepFunctionsParameters`  <a name="cfn-ssm-maintenancewindowtask-taskinvocationparameters-maintenancewindowstepfunctionsparameters"></a>
The parameters for a `STEP_FUNCTIONS` task type\.  
*Required*: No  
*Type*: [MaintenanceWindowStepFunctionsParameters](aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)