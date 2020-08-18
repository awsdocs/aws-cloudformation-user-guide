# AWS::SSM::MaintenanceWindowTask MaintenanceWindowRunCommandParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters"></a>

The `MaintenanceWindowRunCommandParameters` property type specifies the parameters for a `RUN_COMMAND` task type for a maintenance window task in AWS Systems Manager\. This means that these parameters are the same as those for the `SendCommand` API call\. For more information, see [SendCommand](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_SendCommand.html) in the *AWS Systems Manager API Reference*\.

 `MaintenanceWindowRunCommandParameters` is a property of the [TaskInvocationParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.html) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-syntax.json"></a>

```
{
  "[Comment](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-comment)" : String,
  "[DocumentHash](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthash)" : String,
  "[DocumentHashType](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthashtype)" : String,
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
  [Comment](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-comment): String
  [DocumentHash](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthash): String
  [DocumentHashType](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthashtype): String
  [NotificationConfig](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-notificationconfig): 
    NotificationConfig
  [OutputS3BucketName](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3bucketname): String
  [OutputS3KeyPrefix](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3keyprefix): String
  [Parameters](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-parameters): Json
  [ServiceRoleArn](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-servicerolearn): String
  [TimeoutSeconds](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-timeoutseconds): Integer
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-properties"></a>

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

`NotificationConfig`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-notificationconfig"></a>
Configurations for sending notifications about command status changes on a per\-instance basis\.  
*Required*: No  
*Type*: [NotificationConfig](aws-properties-ssm-maintenancewindowtask-notificationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputS3BucketName`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3bucketname"></a>
The name of the S3 bucket\.  
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
The ARN of the IAM service role to use to publish Amazon Simple Notification Service \(Amazon SNS\) notifications for maintenance window Run Command tasks\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutSeconds`  <a name="cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-timeoutseconds"></a>
If this time is reached and the command has not already started running, it doesn't run\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `30`  
*Maximum*: `2592000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)