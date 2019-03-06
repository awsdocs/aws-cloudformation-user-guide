# Amazon FSx FileSystem WindowsConfiguration<a name="aws-properties-fsx-filesystem-windowsconfiguration"></a>

<a name="aws-properties-fsx-filesystem-windowsconfiguration-description"></a>The `WindowsConfiguration` property type defines an Amazon FSx for Windows File Server file system\.

<a name="aws-properties-fsx-filesystem-windowsconfiguration-inheritance"></a> `WindowsConfiguration` is a property of the [AWS::FSx::FileSystem](aws-resource-fsx-filesystem.md) resource\.

## Syntax<a name="aws-properties-fsx-filesystem-windowsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax\.

### JSON<a name="aws-properties-fsx-filesystem-windowsconfiguration-syntax.json"></a>

```
{
  "[ActiveDirectoryId](#cfn-fsx-filesystem-windowsconfiguration-activedirectoryid)" : String,
  "[AutomaticBackupRetentionDays](#cfn-fsx-filesystem-windowsconfiguration-automaticbackupretentiondays)" : Integer,
  "[CopyTagsToBackups](#cfn-fsx-filesystem-windowsconfiguration-copytagstobackups)" : Boolean,
  "[DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-windowsconfiguration-dailyautomaticbackupstarttime)" : String,
  "[ThroughputCapacity](#cfn-fsx-filesystem-windowsconfiguration-throughputcapacity)" : Integer,
  "[WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-windowsconfiguration-weeklymaintenancestarttime)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-windowsconfiguration-syntax.yaml"></a>

```
[ActiveDirectoryId](#cfn-fsx-filesystem-windowsconfiguration-activedirectoryid): String
[AutomaticBackupRetentionDays](#cfn-fsx-filesystem-windowsconfiguration-automaticbackupretentiondays): Integer
[CopyTagsToBackups](#cfn-fsx-filesystem-windowsconfiguration-copytagstobackups): Boolean
[DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-windowsconfiguration-dailyautomaticbackupstarttime): String
[ThroughputCapacity](#cfn-fsx-filesystem-windowsconfiguration-throughputcapacity): Integer
[WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-windowsconfiguration-weeklymaintenancestarttime): String
```

## Properties<a name="aws-properties-fsx-filesystem-windowsconfiguration-properties"></a>

`ActiveDirectoryId`  <a name="cfn-fsx-filesystem-windowsconfiguration-activedirectoryid"></a>
The ID for an existing Microsoft Active Directory instance that the file system should join when it's created\.  
Length Constraints: Fixed length of 12\. Pattern: ^d\-\[0\-9a\-f\]\{10\}$  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`AutomaticBackupRetentionDays`  <a name="cfn-fsx-filesystem-windowsconfiguration-automaticbackupretentiondays"></a>
The number of days to retain automatic backups\. The default is to retain backups for 7 days\. Setting this value to 0 disables the creation of automatic backups\. The maximum retention period for backups is 35 days\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CopyTagsToBackups`  <a name="cfn-fsx-filesystem-windowsconfiguration-copytagstobackups"></a>
A boolean flag indicating whether tags on the file system should be copied to backups\. This value defaults to false\. If it's set to true, all tags on the file system are copied to all automatic backups and any user\-initiated backups where the user doesn't specify any tags\. If this value is true, and you specify one or more tags, only the specified tags are copied to backups\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DailyAutomaticBackupStartTime`  <a name="cfn-fsx-filesystem-windowsconfiguration-dailyautomaticbackupstarttime"></a>
The preferred time to take daily automatic backups, in the UTC time zone\.  
Length Constraints: Fixed length of 5\. Pattern: ^\(\[01\]\\d\|2\[0\-3\]\):?\(\[0\-5\]\\d\)$  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ThroughputCapacity`  <a name="cfn-fsx-filesystem-windowsconfiguration-throughputcapacity"></a>
The throughput of an Amazon FSx file system, measured in megabytes per second\. Valid range of values: Minimum value of 8\. Maximum value of 2048\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`WeeklyMaintenanceStartTime`  <a name="cfn-fsx-filesystem-windowsconfiguration-weeklymaintenancestarttime"></a>
The preferred start time to perform weekly maintenance, in the UTC time zone\.  
Length Constraints: Fixed length of 7\. Pattern: ^\[1\-7\]:\(\[01\]\\d\|2\[0\-3\]\):?\(\[0\-5\]\\d\)$  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-fsx-filesystem-windowsconfiguration-seealso"></a>
+ [CreateFileSystemWindowsConfiguration](https://docs.aws.amazon.com/fsx/latest/APIReference/API_CreateFileSystemWindowsConfiguration.html) in the *Amazon FSx API Reference*