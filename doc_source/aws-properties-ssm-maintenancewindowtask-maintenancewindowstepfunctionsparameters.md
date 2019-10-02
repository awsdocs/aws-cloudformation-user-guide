# AWS::SSM::MaintenanceWindowTask MaintenanceWindowStepFunctionsParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters"></a>

The `MaintenanceWindowStepFunctionsParameters` property type specifies the parameters for execution of the `STEP_FUNCTION` for a maintenance window task in AWS Systems Manager\.

 `MaintenanceWindowStepFunctionsParameters` is a property of the [TaskInvocationParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.html) property type\.

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
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowstepfunctionsparameters-name"></a>
The name of the `STEP_FUNCTION` task\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `80`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
