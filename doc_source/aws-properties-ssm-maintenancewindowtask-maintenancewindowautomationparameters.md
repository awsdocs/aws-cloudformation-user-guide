# Amazon EC2 Systems Manager MaintenanceWindowTask MaintenanceWindowAutomationParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-description"></a>The `MaintenanceWindowAutomationParameters` property type specifies the parameters for an `AUTOMATION` task type for an Amazon EC2 Systems Manager Maintenance Window task\.

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-inheritance"></a> `MaintenanceWindowAutomationParameters` is a property of the [SSM MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters)" : JSON object,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-documentversion)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-parameters):
  JSON object
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowautomationparameters-documentversion): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowautomationparameters-properties"></a>

`Parameters`  
The parameters for the `AUTOMATION` task\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: No interruption 

`DocumentVersion`  
The version of an Automation document to use during task execution\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 