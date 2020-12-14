# AWS::AppSync::Resolver LambdaConflictHandlerConfig<a name="aws-properties-appsync-resolver-lambdaconflicthandlerconfig"></a>

The `LambdaConflictHandlerConfig` when configuring LAMBDA as the Conflict Handler\.

## Syntax<a name="aws-properties-appsync-resolver-lambdaconflicthandlerconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-resolver-lambdaconflicthandlerconfig-syntax.json"></a>

```
{
  "[LambdaConflictHandlerArn](#cfn-appsync-resolver-lambdaconflicthandlerconfig-lambdaconflicthandlerarn)" : String
}
```

### YAML<a name="aws-properties-appsync-resolver-lambdaconflicthandlerconfig-syntax.yaml"></a>

```
  [LambdaConflictHandlerArn](#cfn-appsync-resolver-lambdaconflicthandlerconfig-lambdaconflicthandlerarn): String
```

## Properties<a name="aws-properties-appsync-resolver-lambdaconflicthandlerconfig-properties"></a>

`LambdaConflictHandlerArn`  <a name="cfn-appsync-resolver-lambdaconflicthandlerconfig-lambdaconflicthandlerarn"></a>
The Arn for the Lambda function to use as the Conflict Handler\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)