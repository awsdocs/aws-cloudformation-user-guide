# AWS::AppSync::FunctionConfiguration SyncConfig<a name="aws-properties-appsync-functionconfiguration-syncconfig"></a>

Describes a Sync configuration for a resolver\.

Contains information on which Conflict Detection as well as Resolution strategy should be performed when the resolver is invoked\.

## Syntax<a name="aws-properties-appsync-functionconfiguration-syncconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-functionconfiguration-syncconfig-syntax.json"></a>

```
{
  "[ConflictDetection](#cfn-appsync-functionconfiguration-syncconfig-conflictdetection)" : String,
  "[ConflictHandler](#cfn-appsync-functionconfiguration-syncconfig-conflicthandler)" : String,
  "[LambdaConflictHandlerConfig](#cfn-appsync-functionconfiguration-syncconfig-lambdaconflicthandlerconfig)" : LambdaConflictHandlerConfig
}
```

### YAML<a name="aws-properties-appsync-functionconfiguration-syncconfig-syntax.yaml"></a>

```
  [ConflictDetection](#cfn-appsync-functionconfiguration-syncconfig-conflictdetection): String
  [ConflictHandler](#cfn-appsync-functionconfiguration-syncconfig-conflicthandler): String
  [LambdaConflictHandlerConfig](#cfn-appsync-functionconfiguration-syncconfig-lambdaconflicthandlerconfig): 
    LambdaConflictHandlerConfig
```

## Properties<a name="aws-properties-appsync-functionconfiguration-syncconfig-properties"></a>

`ConflictDetection`  <a name="cfn-appsync-functionconfiguration-syncconfig-conflictdetection"></a>
The Conflict Detection strategy to use\.  
+  **VERSION**: Detect conflicts based on object versions for this resolver\.
+  **NONE**: Do not detect conflicts when executing this resolver\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConflictHandler`  <a name="cfn-appsync-functionconfiguration-syncconfig-conflicthandler"></a>
The Conflict Resolution strategy to perform in the event of a conflict\.  
+  **OPTIMISTIC\_CONCURRENCY**: Resolve conflicts by rejecting mutations when versions do not match the latest version at the server\.
+  **AUTOMERGE**: Resolve conflicts with the Automerge conflict resolution strategy\.
+  **LAMBDA**: Resolve conflicts with a Lambda function supplied in the LambdaConflictHandlerConfig\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaConflictHandlerConfig`  <a name="cfn-appsync-functionconfiguration-syncconfig-lambdaconflicthandlerconfig"></a>
The `LambdaConflictHandlerConfig` when configuring LAMBDA as the Conflict Handler\.  
*Required*: No  
*Type*: [LambdaConflictHandlerConfig](aws-properties-appsync-functionconfiguration-lambdaconflicthandlerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)