# AWS::DataSync::Task Options<a name="aws-properties-datasync-task-options"></a>

Represents the options that are available to control the behavior of a [StartTaskExecution](https://docs.aws.amazon.com/datasync/latest/userguide/API_StartTaskExecution.html) operation\. This behavior includes preserving metadata, such as user ID \(UID\), group ID \(GID\), and file permissions; overwriting files in the destination; data integrity verification; and so on\.

A task has a set of default options associated with it\. If you don't specify an option in [StartTaskExecution](https://docs.aws.amazon.com/datasync/latest/userguide/API_StartTaskExecution.html), the default value is used\. You can override the default options on each task execution by specifying an overriding `Options` value to [StartTaskExecution](https://docs.aws.amazon.com/datasync/latest/userguide/API_StartTaskExecution.html)\.

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
  "[ObjectTags](#cfn-datasync-task-options-objecttags)" : String,
  "[OverwriteMode](#cfn-datasync-task-options-overwritemode)" : String,
  "[PosixPermissions](#cfn-datasync-task-options-posixpermissions)" : String,
  "[PreserveDeletedFiles](#cfn-datasync-task-options-preservedeletedfiles)" : String,
  "[PreserveDevices](#cfn-datasync-task-options-preservedevices)" : String,
  "[SecurityDescriptorCopyFlags](#cfn-datasync-task-options-securitydescriptorcopyflags)" : String,
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
  [ObjectTags](#cfn-datasync-task-options-objecttags): String
  [OverwriteMode](#cfn-datasync-task-options-overwritemode): String
  [PosixPermissions](#cfn-datasync-task-options-posixpermissions): String
  [PreserveDeletedFiles](#cfn-datasync-task-options-preservedeletedfiles): String
  [PreserveDevices](#cfn-datasync-task-options-preservedevices): String
  [SecurityDescriptorCopyFlags](#cfn-datasync-task-options-securitydescriptorcopyflags): String
  [TaskQueueing](#cfn-datasync-task-options-taskqueueing): String
  [TransferMode](#cfn-datasync-task-options-transfermode): String
  [Uid](#cfn-datasync-task-options-uid): String
  [VerifyMode](#cfn-datasync-task-options-verifymode): String
```

## Properties<a name="aws-properties-datasync-task-options-properties"></a>

`Atime`  <a name="cfn-datasync-task-options-atime"></a>
A file metadata value that shows the last time that a file was accessed \(that is, when the file was read or written to\)\. If you set `Atime` to `BEST_EFFORT`, AWS DataSync attempts to preserve the original `Atime` attribute on all source files \(that is, the version before the PREPARING phase\)\. However, `Atime`'s behavior is not fully standard across platforms, so AWS DataSync can only do this on a best\-effort basis\.   
Default value: `BEST_EFFORT`  
`BEST_EFFORT`: Attempt to preserve the per\-file `Atime` value \(recommended\)\.  
`NONE`: Ignore `Atime`\.  
If `Atime` is set to `BEST_EFFORT`, `Mtime` must be set to `PRESERVE`\.   
If `Atime` is set to `NONE`, `Mtime` must also be `NONE`\. 
*Required*: No  
*Type*: String  
*Allowed values*: `BEST_EFFORT | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BytesPerSecond`  <a name="cfn-datasync-task-options-bytespersecond"></a>
A value that limits the bandwidth used by AWS DataSync\. For example, if you want AWS DataSync to use a maximum of 1 MB, set this value to `1048576` \(=1024\*1024\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Gid`  <a name="cfn-datasync-task-options-gid"></a>
The group ID \(GID\) of the file's owners\.   
Default value: `INT_VALUE`  
`INT_VALUE`: Preserve the integer value of the user ID \(UID\) and group ID \(GID\) \(recommended\)\.  
`NAME`: Currently not supported\.  
`NONE`: Ignore the UID and GID\.   
*Required*: No  
*Type*: String  
*Allowed values*: `BOTH | INT_VALUE | NAME | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogLevel`  <a name="cfn-datasync-task-options-loglevel"></a>
Specifies the type of logs that DataSync publishes to a Amazon CloudWatch Logs log group\. To specify the log group, see [CloudWatchLogGroupArn](https://docs.aws.amazon.com/datasync/latest/userguide/API_CreateTask.html#DataSync-CreateTask-request-CloudWatchLogGroupArn)\.  
If you set `LogLevel` to `OFF`, no logs are published\. `BASIC` publishes logs on errors for individual files transferred\. `TRANSFER` publishes logs for every file or object that is transferred and integrity checked\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BASIC | OFF | TRANSFER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mtime`  <a name="cfn-datasync-task-options-mtime"></a>
A value that indicates the last time that a file was modified \(that is, a file was written to\) before the PREPARING phase\. This option is required for cases when you need to run the same task more than one time\.   
Default value: `PRESERVE`   
`PRESERVE`: Preserve original `Mtime` \(recommended\)  
 `NONE`: Ignore `Mtime`\.   
If `Mtime` is set to `PRESERVE`, `Atime` must be set to `BEST_EFFORT`\.  
If `Mtime` is set to `NONE`, `Atime` must also be set to `NONE`\. 
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | PRESERVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectTags`  <a name="cfn-datasync-task-options-objecttags"></a>
Specifies whether object tags are preserved when transferring between object storage systems\. If you want your DataSync task to ignore object tags, specify the `NONE` value\.  
Default Value: `PRESERVE`   
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | PRESERVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OverwriteMode`  <a name="cfn-datasync-task-options-overwritemode"></a>
Specifies whether data at the destination location should be overwritten or preserved\. If set to `NEVER`, a destination file for example will not be replaced by a source file \(even if the destination file differs from the source file\)\. If you modify files in the destination and you sync the files, you can use this value to protect against overwriting those changes\.   
Some storage classes have specific behaviors that can affect your Amazon S3 storage cost\. For detailed information, see [Considerations when working with Amazon S3 storage classes in DataSync](https://docs.aws.amazon.com/datasync/latest/userguide/create-s3-location.html#using-storage-classes)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ALWAYS | NEVER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PosixPermissions`  <a name="cfn-datasync-task-options-posixpermissions"></a>
A value that determines which users or groups can access a file for a specific purpose, such as reading, writing, or execution of the file\. This option should be set only for Network File System \(NFS\), Amazon EFS, and Amazon S3 locations\. For more information about what metadata is copied by DataSync, see [Metadata Copied by DataSync](https://docs.aws.amazon.com/datasync/latest/userguide/special-files.html#metadata-copied)\.   
Default value: `PRESERVE`  
`PRESERVE`: Preserve POSIX\-style permissions \(recommended\)\.  
`NONE`: Ignore permissions\.   
 AWS DataSync can preserve extant permissions of a source location\.
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | PRESERVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreserveDeletedFiles`  <a name="cfn-datasync-task-options-preservedeletedfiles"></a>
A value that specifies whether files in the destination that don't exist in the source file system are preserved\. This option can affect your storage costs\. If your task deletes objects, you might incur minimum storage duration charges for certain storage classes\. For detailed information, see [Considerations when working with Amazon S3 storage classes in DataSync ](https://docs.aws.amazon.com/datasync/latest/userguide/create-s3-location.html#using-storage-classes) in the * AWS DataSync User Guide*\.  
Default value: `PRESERVE`  
`PRESERVE`: Ignore destination files that aren't present in the source \(recommended\)\.   
`REMOVE`: Delete destination files that aren't present in the source\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PRESERVE | REMOVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreserveDevices`  <a name="cfn-datasync-task-options-preservedevices"></a>
A value that determines whether AWS DataSync should preserve the metadata of block and character devices in the source file system, and re\-create the files with that device name and metadata on the destination\. DataSync does not copy the contents of such devices, only the name and metadata\.   
 AWS DataSync can't sync the actual contents of such devices, because they are nonterminal and don't return an end\-of\-file \(EOF\) marker\.
Default value: `NONE`  
`NONE`: Ignore special devices \(recommended\)\.   
`PRESERVE`: Preserve character and block device metadata\. This option isn't currently supported for Amazon EFS\.   
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | PRESERVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityDescriptorCopyFlags`  <a name="cfn-datasync-task-options-securitydescriptorcopyflags"></a>
A value that determines which components of the SMB security descriptor are copied from source to destination objects\.   
This value is only used for transfers between SMB and Amazon FSx for Windows File Server locations, or between two Amazon FSx for Windows File Server locations\. For more information about how DataSync handles metadata, see [How DataSync Handles Metadata and Special Files](https://docs.aws.amazon.com/datasync/latest/userguide/special-files.html)\.   
Default value: `OWNER_DACL`  
 `OWNER_DACL`: For each copied object, DataSync copies the following metadata:  
+ Object owner\.
+ NTFS discretionary access control lists \(DACLs\), which determine whether to grant access to an object\.
When you use option, DataSync does NOT copy the NTFS system access control lists \(SACLs\), which are used by administrators to log attempts to access a secured object\.  
 `OWNER_DACL_SACL`: For each copied object, DataSync copies the following metadata:  
+ Object owner\.
+ NTFS discretionary access control lists \(DACLs\), which determine whether to grant access to an object\.
+ NTFS system access control lists \(SACLs\), which are used by administrators to log attempts to access a secured object\.
Copying SACLs requires granting additional permissions to the Windows user that DataSync uses to access your SMB location\. For information about choosing a user that ensures sufficient permissions to files, folders, and metadata, see [user](https://docs.aws.amazon.com/datasync/latest/userguide/create-smb-location.html#SMBuser)\.  
`NONE`: None of the SMB security descriptor components are copied\. Destination objects are owned by the user that was provided for accessing the destination location\. DACLs and SACLs are set based on the destination server’s configuration\.   
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | OWNER_DACL | OWNER_DACL_SACL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskQueueing`  <a name="cfn-datasync-task-options-taskqueueing"></a>
Specifies whether tasks should be queued before executing the tasks\. The default is `ENABLED`, which means the tasks will be queued\.  
If you use the same agent to run multiple tasks, you can enable the tasks to run in series\. For more information, see [Queueing task executions](https://docs.aws.amazon.com/datasync/latest/userguide/run-task.html#queue-task-execution)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransferMode`  <a name="cfn-datasync-task-options-transfermode"></a>
A value that determines whether DataSync transfers only the data and metadata that differ between the source and the destination location, or whether DataSync transfers all the content from the source, without comparing it to the destination location\.   
`CHANGED`: DataSync copies only data or metadata that is new or different from the source location to the destination location\.  
`ALL`: DataSync copies all source location content to the destination, without comparing it to existing content on the destination\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ALL | CHANGED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uid`  <a name="cfn-datasync-task-options-uid"></a>
The user ID \(UID\) of the file's owner\.   
Default value: `INT_VALUE`  
`INT_VALUE`: Preserve the integer value of the UID and group ID \(GID\) \(recommended\)\.  
`NAME`: Currently not supported  
`NONE`: Ignore the UID and GID\.   
*Required*: No  
*Type*: String  
*Allowed values*: `BOTH | INT_VALUE | NAME | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerifyMode`  <a name="cfn-datasync-task-options-verifymode"></a>
A value that determines whether a data integrity verification is performed at the end of a task execution after all data and metadata have been transferred\. For more information, see [Configure task settings](https://docs.aws.amazon.com/datasync/latest/userguide/create-task.html)\.   
Default value: `POINT_IN_TIME_CONSISTENT`  
`ONLY_FILES_TRANSFERRED` \(recommended\): Perform verification only on files that were transferred\.   
`POINT_IN_TIME_CONSISTENT`: Scan the entire source and entire destination at the end of the transfer to verify that the source and destination are fully synchronized\. This option isn't supported when transferring to S3 Glacier or S3 Glacier Deep Archive storage classes\.  
`NONE`: No additional verification is done at the end of the transfer, but all data transmissions are integrity\-checked with checksum verification during the transfer\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | ONLY_FILES_TRANSFERRED | POINT_IN_TIME_CONSISTENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)