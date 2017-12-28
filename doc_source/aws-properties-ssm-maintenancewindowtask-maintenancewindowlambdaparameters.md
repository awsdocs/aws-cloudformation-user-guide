# Amazon EC2 Systems Manager MaintenanceWindowTask MaintenanceWindowLambdaParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-description"></a>The `MaintenanceWindowLambdaParameters` property type specifies the parameters for a `LAMBDA` task type for an Amazon EC2 Systems Manager Maintenance Window task\.

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-inheritance"></a> `MaintenanceWindowLambdaParameters` is a property of the [SSM MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-clientcontext)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-qualifier)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-payload)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-clientcontext): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-qualifier): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-payload): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-properties"></a>

`ClientContext`  
Client\-specific information to pass to the Lambda function that you're invoking\. You can then use the `context` variable to process the client information in your Lambda function\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Qualifier`  
A Lambda function version or alias name\. If you specify a function version, the action uses the qualified function Amazon Resource Name \(ARN\) to invoke a specific Lambda function\. If you specify an alias name, the action uses the alias ARN to invoke the Lambda function version that the alias points to\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Payload`  
JSON to provide to your Lambda function as input\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 