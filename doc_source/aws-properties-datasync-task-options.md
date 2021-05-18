# AWS::DataSync::Task Options<a name="aws-properties-datasync-task-options"></a>

Represents the options that are available to control the behavior of a [StartTaskExecution](https://docs.aws.amazon.com/datasync/latest/userguide/API_StartTaskExecution.html) operation\. Behavior includes preserving metadata such as user ID \(UID\), group ID \(GID\), and file permissions, and also overwriting files in the destination, data integrity verification, and so on\.

A task has a set of default options associated with it\. If you don't specify an option in [StartTaskExecution](https://docs.aws.amazon.com/datasync/latest/userguide/API_StartTaskExecution.html), the default value is used\. You can override the defaults options on each task execution by specifying an overriding `Options` value to [StartTaskExecution](https://docs.aws.amazon.com/datasync/latest/userguide/API_StartTaskExecution.html)\.

## Syntax<a name="aws-properties-datasync-task-options-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-options-syntax.json"></a>

```
{
  "[Atime](#cfn-datasync-task-options-atime)" : String,
  "[BytesPerSecond](#cfn-datasync-task-options-bytespersecond)" : Integer,
  "[Gid](#cfn-datasync-task-options-gid)" : String,
  "[LogLevel](#cfn-datasync-task-options-loglevel)" : String,
  "[Mtime](#cfn-datasync-task-options-mtime)" : String,
  "[OverwriteMode](#cfn-datasync-task-options-overwritemode)" : String,
  "[PosixPermissions](#cfn-datasync-task-options-posixpermissions)" : String,
  "[PreserveDeletedFiles](#cfn-datasync-task-options-preservedeletedfiles)" : String,
  "[PreserveDevices](#cfn-datasync-task-options-preservedevices)" : String,
  "[TaskQueueing](#cfn-datasync-task-options-taskqueueing)" : String,
  "[TransferMode](#cfn-datasync-task-options-transfermode)" : String,
  "[Uid](#cfn-datasync-task-options-uid)" : String,
  "[VerifyMode](#cfn-datasync-task-options-verifymode)" : String
}
```

### YAML<a name="aws-properties-datasync-task-options-syntax.yaml"></a>

```
  [Atime](#cfn-datasync-task-options-atime): String
  [BytesPerSecond](#cfn-datasync-task-options-bytespersecond): Integer
  [Gid](#cfn-datasync-task-options-gid): String
  [LogLevel](#cfn-datasync-task-options-loglevel): String
  [Mtime](#cfn-datasync-task-options-mtime): String
  [OverwriteMode](#cfn-datasync-task-options-overwritemode): String
  [PosixPermissions](#cfn-datasync-task-options-posixpermissions): String
  [PreserveDeletedFiles](#cfn-datasync-task-options-preservedeletedfiles): String
  [PreserveDevices](#cfn-datasync-task-options-preservedevices): String
  [TaskQueueing](#cfn-datasync-task-options-taskqueueing): String
  [TransferMode](#cfn-datasync-task-options-transfermode): String
  [Uid](#cfn-datasync-task-options-uid): String
  [VerifyMode](#cfn-datasync-task-options-verifymode): String
```

## Properties<a name="aws-properties-datasync-task-options-properties"></a>

`Atime`  <a name="cfn-datasync-task-options-atime"></a>
A file metadata value that shows the last time a file was accessed \(that is, when the file was read or written to\)\. If you set `Atime` to BEST\_EFFORT, DataSync attempts to preserve the original `Atime` attribute on all source files \(that is, the version before the PREPARING phase\)\. However, `Atime`'s behavior is not fully standard across platforms, so AWS DataSync can only do this on a best\-effort basis\.   
Default value: BEST\_EFFORT\.  
BEST\_EFFORT: Attempt to preserve the per\-file `Atime` value \(recommended\)\.  
NONE: Ignore `Atime`\.  
If `Atime` is set to BEST\_EFFORT, `Mtime` must be set to PRESERVE\.   
If `Atime` is set to NONE, `Mtime` must also be NONE\. 
*Required*: No  
*Type*: String  
*Allowed values*: `BEST_EFFORT | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BytesPerSecond`  <a name="cfn-datasync-task-options-bytespersecond"></a>
A value that limits the bandwidth used by AWS DataSync\. For example, if you want AWS DataSync to use a maximum of 1 MB, set this value to `1048576` \(`=1024*1024`\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Gid`  <a name="cfn-datasync-task-options-gid"></a>
The group ID \(GID\) of the file's owners\.   
Default value: INT\_VALUE\. This preserves the integer value of the ID\.  
INT\_VALUE: Preserve the integer value of UID and group ID \(GID\) \(recommended\)\.  
NAME: Currently not supported  
NONE: Ignore UID and GID\.   
*Required*: No  
*Type*: String  
*Allowed values*: `BOTH | INT_VALUE | NAME | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogLevel`  <a name="cfn-datasync-task-options-loglevel"></a>
A value that determines the type of logs that DataSync publishes to a log stream in the Amazon CloudWatch log group that you provide\. For more information about providing a log group for DataSync, see [CloudWatchLogGroupArn](https://docs.aws.amazon.com/datasync/latest/userguide/API_CreateTask.html#DataSync-CreateTask-request-CloudWatchLogGroupArn)\. If set to `OFF`, no logs are published\. `BASIC` publishes logs on errors for individual files transferred, and `TRANSFER` publishes logs for every file or object that is transferred and integrity checked\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BASIC | OFF | TRANSFER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mtime`  <a name="cfn-datasync-task-options-mtime"></a>
A value that indicates the last time that a file was modified \(that is, a file was written to\) before the PREPARING phase\.   
Default value: PRESERVE\.   
PRESERVE: Preserve original `Mtime` \(recommended\)  
 NONE: Ignore `Mtime`\.   
If `Mtime` is set to PRESERVE, `Atime` must be set to BEST\_EFFORT\.  
If `Mtime` is set to NONE, `Atime` must also be set to NONE\. 
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | PRESERVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OverwriteMode`  <a name="cfn-datasync-task-options-overwritemode"></a>
A value that determines whether files at the destination should be overwritten or preserved when copying files\. If set to `NEVER` a destination file will not be replaced by a source file, even if the destination file differs from the source file\. If you modify files in the destination and you sync the files, you can use this value to protect against overwriting those changes\.   
Some storage classes have specific behaviors that can affect your S3 storage cost\. For detailed information, see [Considerations when working with Amazon S3 storage classes in DataSync ](https://docs.aws.amazon.com/datasync/latest/userguide/create-s3-location.html#using-storage-classes) in the *AWS DataSync User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ALWAYS | NEVER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PosixPermissions`  <a name="cfn-datasync-task-options-posixpermissions"></a>
A value that determines which users or groups can access a file for a specific purpose such as reading, writing, or execution of the file\.   
Default value: PRESERVE\.  
PRESERVE: Preserve POSIX\-style permissions \(recommended\)\.  
NONE: Ignore permissions\.   
AWS DataSync can preserve extant permissions of a source location\.
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | PRESERVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreserveDeletedFiles`  <a name="cfn-datasync-task-options-preservedeletedfiles"></a>
A value that specifies whether files in the destination that don't exist in the source file system should be preserved\. This option can affect your storage cost\. If your task deletes objects, you might incur minimum storage duration charges for certain storage classes\. For detailed information, see [Considerations when working with Amazon S3 storage classes in DataSync ](https://docs.aws.amazon.com/datasync/latest/userguide/create-s3-location.html#using-storage-classes) in the *AWS DataSync User Guide*\.  
Default value: PRESERVE\.  
PRESERVE: Ignore such destination files \(recommended\)\.   
REMOVE: Delete destination files that aren’t present in the source\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PRESERVE | REMOVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreserveDevices`  <a name="cfn-datasync-task-options-preservedevices"></a>
A value that determines whether AWS DataSync should preserve the metadata of block and character devices in the source file system, and recreate the files with that device name and metadata on the destination\.  
AWS DataSync can't sync the actual contents of such devices, because they are nonterminal and don't return an end\-of\-file \(EOF\) marker\.
Default value: NONE\.  
NONE: Ignore special devices \(recommended\)\.   
PRESERVE: Preserve character and block device metadata\. This option isn't currently supported for Amazon EFS\.   
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | PRESERVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskQueueing`  <a name="cfn-datasync-task-options-taskqueueing"></a>
A value that determines whether tasks should be queued before executing the tasks\. If set to `ENABLED`, the tasks will be queued\. The default is `ENABLED`\.  
If you use the same agent to run multiple tasks, you can enable the tasks to run in series\. For more information, see [Queueing task executions](https://docs.aws.amazon.com/datasync/latest/userguide/run-task.html#queue-task-execution)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransferMode`  <a name="cfn-datasync-task-options-transfermode"></a>
A value that determines whether DataSync transfers only the data and metadata that differ between the source and the destination location, or whether DataSync transfers all the content from the source, without comparing to the destination location\.   
CHANGED: DataSync copies only data or metadata that is new or different content from the source location to the destination location\.  
ALL: DataSync copies all source location content to the destination, without comparing to existing content on the destination\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ALL | CHANGED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uid`  <a name="cfn-datasync-task-options-uid"></a>
The user ID \(UID\) of the file's owner\.   
Default value: INT\_VALUE\. This preserves the integer value of the ID\.  
INT\_VALUE: Preserve the integer value of UID and group ID \(GID\) \(recommended\)\.  
NAME: Currently not supported  
NONE: Ignore UID and GID\.   
*Required*: No  
*Type*: String  
*Allowed values*: `BOTH | INT_VALUE | NAME | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerifyMode`  <a name="cfn-datasync-task-options-verifymode"></a>
A value that determines whether a data integrity verification should be performed at the end of a task execution after all data and metadata have been transferred\. For more information, see [Configure task settings](https://docs.aws.amazon.com/datasync/latest/userguide/create-task.html)\.   
Default value: POINT\_IN\_TIME\_CONSISTENT\.  
ONLY\_FILES\_TRANSFERRED \(recommended\): Perform verification only on files that were transferred\.   
POINT\_IN\_TIME\_CONSISTENT: Scan the entire source and entire destination at the end of the transfer to verify that source and destination are fully synchronized\. This option isn't supported when transferring to S3 Glacier or S3 Glacier Deep Archive storage classes\.  
NONE: No additional verification is done at the end of the transfer, but all data transmissions are integrity\-checked with checksum verification during the transfer\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | ONLY_FILES_TRANSFERRED | POINT_IN_TIME_CONSISTENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)