# AWS::SSM::MaintenanceWindowTask MaintenanceWindowLambdaParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters"></a>

The `MaintenanceWindowLambdaParameters` property type specifies the parameters for a `LAMBDA` task type for a maintenance window task in AWS Systems Manager\.

 `MaintenanceWindowLambdaParameters` is a property of the [TaskInvocationParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.html) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax.json"></a>

```
{
  "[ClientContext](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-clientcontext)" : String,
  "[Payload](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-payload)" : String,
  "[Qualifier](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-qualifier)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-syntax.yaml"></a>

```
  [ClientContext](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-clientcontext): String
  [Payload](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-payload): String
  [Qualifier](#cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-qualifier): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-properties"></a>

`ClientContext`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-clientcontext"></a>
Client\-specific information to pass to the Lambda function that you're invoking\. You can then use the `context` variable to process the client information in your Lambda function\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `8000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Payload`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-payload"></a>
JSON to provide to your Lambda function as input\.  
Although `Type` is listed as "String" for this property, the payload content must be formatted as a Base64\-encoded binary data object\.
*Length Constraint:* 4096  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Qualifier`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowlambdaparameters-qualifier"></a>
A Lambda function version or alias name\. If you specify a function version, the action uses the qualified function Amazon Resource Name \(ARN\) to invoke a specific Lambda function\. If you specify an alias name, the action uses the alias ARN to invoke the Lambda function version that the alias points to\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)