# AWS Systems Manager MaintenanceWindowTask MaintenanceWindowLambdaParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-description"></a>The `MaintenanceWindowLambdaParameters` property type specifies the parameters for a `LAMBDA` task type for a Maintenance Window task in AWS Systems Manager\.

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-inheritance"></a> `MaintenanceWindowLambdaParameters` is a property of the [Systems Manager MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax.json"></a>

```
{
  "[ClientContext](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-clientcontext)" : String,
  "[Qualifier](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-qualifier)" : String,
  "[Payload](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-payload)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax.yaml"></a>

```
[ClientContext](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-clientcontext): String
[Qualifier](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-qualifier): String
[Payload](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-payload): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-properties"></a>

`ClientContext`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-clientcontext"></a>
Client\-specific information to pass to the Lambda function that you're invoking\. You can then use the `context` variable to process the client information in your Lambda function\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Qualifier`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-qualifier"></a>
A Lambda function version or alias name\. If you specify a function version, the action uses the qualified function Amazon Resource Name \(ARN\) to invoke a specific Lambda function\. If you specify an alias name, the action uses the alias ARN to invoke the Lambda function version that the alias points to\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Payload`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-payload"></a>
JSON to provide to your Lambda function as input\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 