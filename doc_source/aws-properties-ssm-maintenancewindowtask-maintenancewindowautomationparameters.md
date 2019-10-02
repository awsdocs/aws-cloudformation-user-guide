# AWS::SSM::MaintenanceWindowTask MaintenanceWindowAutomationParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters"></a>

The `MaintenanceWindowAutomationParameters` property type specifies the parameters for an `AUTOMATION` task type for a maintenance window task in AWS Systems Manager\.

 `MaintenanceWindowAutomationParameters` is a property of the [TaskInvocationParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.html) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax.json"></a>

```
{
  "[DocumentVersion](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-documentversion)" : String,
  "[Parameters](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters)" : Json
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax.yaml"></a>

```
  [DocumentVersion](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-documentversion): String
  [Parameters](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters): Json
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-properties"></a>

`DocumentVersion`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-documentversion"></a>
The version of an Automation document to use during task execution\.  
*Required*: No  
*Type*: String  
*Pattern*: `([$]LATEST|[$]DEFAULT|^[1-9][0-9]*$)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters"></a>
The parameters for the AUTOMATION task\.  
*Required*: No  
*Type*: Json  
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
