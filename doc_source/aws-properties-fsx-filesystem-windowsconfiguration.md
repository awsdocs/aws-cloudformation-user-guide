# AWS::FSx::FileSystem WindowsConfiguration<a name="aws-properties-fsx-filesystem-windowsconfiguration"></a>

The configuration for this Microsoft Windows file system\.

## Syntax<a name="aws-properties-fsx-filesystem-windowsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
*Required*: No  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^d-[0-9a-f]{10}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AutomaticBackupRetentionDays`  <a name="cfn-fsx-filesystem-windowsconfiguration-automaticbackupretentiondays"></a>
The number of days to retain automatic backups\. The default is to retain backups for 7 days\. Setting this value to 0 disables the creation of automatic backups\. The maximum retention period for backups is 35 days\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `35`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTagsToBackups`  <a name="cfn-fsx-filesystem-windowsconfiguration-copytagstobackups"></a>
A boolean flag indicating whether tags on the file system should be copied to backups\. This value defaults to false\. If it's set to true, all tags on the file system are copied to all automatic backups and any user\-initiated backups where the user doesn't specify any tags\. If this value is true, and you specify one or more tags, only the specified tags are copied to backups\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DailyAutomaticBackupStartTime`  <a name="cfn-fsx-filesystem-windowsconfiguration-dailyautomaticbackupstarttime"></a>
The preferred time to take daily automatic backups, in the UTC time zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThroughputCapacity`  <a name="cfn-fsx-filesystem-windowsconfiguration-throughputcapacity"></a>
The throughput of an Amazon FSx file system, measured in megabytes per second, in 2 to the nth increments, between 2^3 \(8\) and 2^11 \(2048\)\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `8`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WeeklyMaintenanceStartTime`  <a name="cfn-fsx-filesystem-windowsconfiguration-weeklymaintenancestarttime"></a>
The preferred start time to perform weekly maintenance, in the UTC time zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-2`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
