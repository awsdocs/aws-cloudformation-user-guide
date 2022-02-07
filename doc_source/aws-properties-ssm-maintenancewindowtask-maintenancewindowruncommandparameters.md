# AWS::SSM::MaintenanceWindowTask MaintenanceWindowRunCommandParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters"></a>

The `MaintenanceWindowRunCommandParameters` property type specifies the parameters for a `RUN_COMMAND` task type for a maintenance window task in AWS Systems Manager\. This means that these parameters are the same as those for the `SendCommand` API call\. For more information about `SendCommand` parameters, see [SendCommand](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_SendCommand.html) in the *AWS Systems Manager API Reference*\.

For information about available parameters in SSM Command documents, you can view the content of the document itself in the Systems Manager console\. For information, see [Viewing SSM command document content](https://docs.aws.amazon.com/systems-manager/latest/userguide/viewing-ssm-document-content.html) in the *AWS Systems Manager User Guide*\.

 `MaintenanceWindowRunCommandParameters` is a property of the [TaskInvocationParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.html) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-syntax.json"></a>

```
{
  "[CloudWatchOutputConfig](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-cloudwatchoutputconfig)" : CloudWatchOutputConfig,
  "[Comment](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-comment)" : String,
  "[DocumentHash](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthash)" : String,
  "[DocumentHashType](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthashtype)" : String,
  "[DocumentVersion](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documentversion)" : String,
  "[NotificationConfig](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-notificationconfig)" : NotificationConfig,
  "[OutputS3BucketName](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3bucketname)" : String,
  "[OutputS3KeyPrefix](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3keyprefix)" : String,
  "[Parameters](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-parameters)" : Json,
  "[ServiceRoleArn](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-servicerolearn)" : String,
  "[TimeoutSeconds](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-timeoutseconds)" : Integer
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-syntax.yaml"></a>

```
  [CloudWatchOutputConfig](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-cloudwatchoutputconfig): 
    CloudWatchOutputConfig
  [Comment](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-comment): String
  [DocumentHash](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthash): String
  [DocumentHashType](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthashtype): String
  [DocumentVersion](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documentversion): String
  [NotificationConfig](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-notificationconfig): 
    NotificationConfig
  [OutputS3BucketName](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3bucketname): String
  [OutputS3KeyPrefix](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3keyprefix): String
  [Parameters](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-parameters): Json
  [ServiceRoleArn](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-servicerolearn): String
  [TimeoutSeconds](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-timeoutseconds): Integer
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-properties"></a>

`CloudWatchOutputConfig`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-cloudwatchoutputconfig"></a>
Configuration options for sending command output to Amazon CloudWatch Logs\.  
*Required*: No  
*Type*: [CloudWatchOutputConfig](aws-properties-ssm-maintenancewindowtask-cloudwatchoutputconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Comment`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-comment"></a>
Information about the command or commands to run\.  
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentHash`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthash"></a>
The SHA\-256 or SHA\-1 hash created by the system when the document was created\. SHA\-1 hashes have been deprecated\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentHashType`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthashtype"></a>
The SHA\-256 or SHA\-1 hash type\. SHA\-1 hashes are deprecated\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Sha1 | Sha256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentVersion`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documentversion"></a>
The AWS Systems Manager document \(SSM document\) version to use in the request\. You can specify `$DEFAULT`, `$LATEST`, or a specific version number\. If you run commands by using the AWS CLI, then you must escape the first two options by using a backslash\. If you specify a version number, then you don't need to use the backslash\. For example:  
 `--document-version "\$DEFAULT"`   
 `--document-version "\$LATEST"`   
 `--document-version "3"`   
*Required*: No  
*Type*: String  
*Pattern*: `([$]LATEST|[$]DEFAULT|^[1-9][0-9]*$)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationConfig`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-notificationconfig"></a>
Configurations for sending notifications about command status changes on a per\-managed node basis\.  
*Required*: No  
*Type*: [NotificationConfig](aws-properties-ssm-maintenancewindowtask-notificationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputS3BucketName`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3bucketname"></a>
The name of the Amazon Simple Storage Service \(Amazon S3\) bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputS3KeyPrefix`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3keyprefix"></a>
The S3 bucket subfolder\.  
*Required*: No  
*Type*: String  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-parameters"></a>
The parameters for the `RUN_COMMAND` task execution\.  
The supported parameters are the same as those for the `SendCommand` API call\. For more information, see [SendCommand](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_SendCommand.html) in the *AWS Systems Manager API Reference*\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRoleArn`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-servicerolearn"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) service role to use to publish Amazon Simple Notification Service \(Amazon SNS\) notifications for maintenance window Run Command tasks\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutSeconds`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-timeoutseconds"></a>
If this time is reached and the command hasn't already started running, it doesn't run\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `30`  
*Maximum*: `2592000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)