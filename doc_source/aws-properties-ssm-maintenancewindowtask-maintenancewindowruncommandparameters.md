# Amazon EC2 Systems Manager MaintenanceWindowTask MaintenanceWindowRunCommandParameters<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters"></a>

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-description"></a>The `MaintenanceWindowRunCommandParameters` property type specifies the parameters for a `RUN_COMMAND` task type for an Amazon EC2 Systems Manager Maintenance Window task\.

<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-inheritance"></a> `MaintenanceWindowRunCommandParameters` is a property of the [SSM MaintenanceWindowTask TaskInvocationParameters](aws-properties-ssm-maintenancewindowtask-taskinvocationparameters.md) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-timeoutseconds)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-comment)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3keyprefix)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-parameters)" : JSON object,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthashtype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-servicerolearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-notificationconfig)" : NotificationConfig,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3bucketname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthash)" : String
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-timeoutseconds): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-comment): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3keyprefix): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-parameters):
  JSON object
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthashtype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-servicerolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-notificationconfig):
  NotificationConfig
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-outputs3bucketname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-documenthash): String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-maintenancewindowruncommandparameters-properties"></a>

`TimeoutSeconds`  
If this time is reached and the command hasn't already started executing, it doesn't execute\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: No interruption 

`Comment`  
Information about the command or commands to execute\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`OutputS3KeyPrefix`  
The Amazon S3 bucket subfolder\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Parameters`  
The parameters for the `RUN_COMMAND` task execution\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: No interruption 

`DocumentHashType`  
The SHA\-256 or SHA\-1 hash type\. SHA\-1 hashes are deprecated\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`ServiceRoleArn`  
The IAM service role that's used during task execution\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`NotificationConfig`  
Configurations for sending notifications about command status changes on a per\-instance basis\.  
 *Required*: No  
 *Type*: [SSM MaintenanceWindowTask NotificationConfig](aws-properties-ssm-maintenancewindowtask-notificationconfig.md)  
 *Update requires*: No interruption 

`OutputS3BucketName`  
The name of the Amazon S3 bucket\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`DocumentHash`  
The SHA\-256 or SHA\-1 hash created by the system when the document was created\. SHA\-1 hashes are deprecated\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 