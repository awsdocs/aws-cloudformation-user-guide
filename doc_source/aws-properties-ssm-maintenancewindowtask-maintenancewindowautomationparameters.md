# AWS::SSM::MaintenanceWindowTask MaintenanceWindowAutomationParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters"></a>

The `MaintenanceWindowAutomationParameters` property type specifies the parameters for an `AUTOMATION` task type for a maintenance window task in AWS Systems Manager\.

 `MaintenanceWindowAutomationParameters` is a property of the [TaskInvocationParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.html) property type\.

For information about available parameters in Automation runbooks, you can view the content of the runbook itself in the Systems Manager console\. For information, see [View runbook content](https://docs.aws.amazon.com/systems-manager/latest/userguide/automation-documents-reference-details.html#view-automation-json) in the *AWS Systems Manager User Guide*\.

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
The version of an Automation runbook to use during task execution\.  
*Required*: No  
*Type*: String  
*Pattern*: `([$]LATEST|[$]DEFAULT|^[1-9][0-9]*$)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters"></a>
The parameters for the AUTOMATION task\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)