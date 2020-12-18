# AWS::AppSync::FunctionConfiguration LambdaConflictHandlerConfig<a name="aws-properties-appsync-functionconfiguration-lambdaconflicthandlerconfig"></a>

The `LambdaConflictHandlerConfig` object when configuring LAMBDA as the Conflict Handler\.

## Syntax<a name="aws-properties-appsync-functionconfiguration-lambdaconflicthandlerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-functionconfiguration-lambdaconflicthandlerconfig-syntax.json"></a>

```
{
  "[LambdaConflictHandlerArn](#cfn-appsync-functionconfiguration-lambdaconflicthandlerconfig-lambdaconflicthandlerarn)" : String
}
```

### YAML<a name="aws-properties-appsync-functionconfiguration-lambdaconflicthandlerconfig-syntax.yaml"></a>

```
  [LambdaConflictHandlerArn](#cfn-appsync-functionconfiguration-lambdaconflicthandlerconfig-lambdaconflicthandlerarn): String
```

## Properties<a name="aws-properties-appsync-functionconfiguration-lambdaconflicthandlerconfig-properties"></a>

`LambdaConflictHandlerArn`  <a name="cfn-appsync-functionconfiguration-lambdaconflicthandlerconfig-lambdaconflicthandlerarn"></a>
The Arn for the Lambda function to use as the Conflict Handler\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)