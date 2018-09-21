# AWS Systems Manager MaintenanceWindowTask MaintenanceWindowAutomationParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-description"></a>The `MaintenanceWindowAutomationParameters` property type specifies the parameters for an `AUTOMATION` task type for a Maintenance Window task in AWS Systems Manager \.

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-inheritance"></a> `MaintenanceWindowAutomationParameters` is a property of the [Systems Manager MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax.json"></a>

```
{
  "[Parameters](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters)" : JSON object,
  "[DocumentVersion](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-documentversion)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax.yaml"></a>

```
[Parameters](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters):
  JSON object
[DocumentVersion](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-documentversion): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-properties"></a>

`Parameters`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters"></a>
The parameters for the `AUTOMATION` task\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DocumentVersion`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-documentversion"></a>
The version of an Automation document to use during task execution\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 