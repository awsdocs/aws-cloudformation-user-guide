# AWS::FSx::FileSystem OpenZFSConfiguration<a name="aws-properties-fsx-filesystem-openzfsconfiguration"></a>

The OpenZFS configuration for the file system that's being created\.

## Syntax<a name="aws-properties-fsx-filesystem-openzfsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-openzfsconfiguration-syntax.json"></a>

```
{
  "[AutomaticBackupRetentionDays](#cfn-fsx-filesystem-openzfsconfiguration-automaticbackupretentiondays)" : Integer,
  "[CopyTagsToBackups](#cfn-fsx-filesystem-openzfsconfiguration-copytagstobackups)" : Boolean,
  "[CopyTagsToVolumes](#cfn-fsx-filesystem-openzfsconfiguration-copytagstovolumes)" : Boolean,
  "[DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-openzfsconfiguration-dailyautomaticbackupstarttime)" : String,
  "[DeploymentType](#cfn-fsx-filesystem-openzfsconfiguration-deploymenttype)" : String,
  "[DiskIopsConfiguration](#cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration)" : DiskIopsConfiguration,
  "[RootVolumeConfiguration](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration)" : RootVolumeConfiguration,
  "[ThroughputCapacity](#cfn-fsx-filesystem-openzfsconfiguration-throughputcapacity)" : Integer,
  "[WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-openzfsconfiguration-weeklymaintenancestarttime)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-openzfsconfiguration-syntax.yaml"></a>

```
  [AutomaticBackupRetentionDays](#cfn-fsx-filesystem-openzfsconfiguration-automaticbackupretentiondays): Integer
  [CopyTagsToBackups](#cfn-fsx-filesystem-openzfsconfiguration-copytagstobackups): Boolean
  [CopyTagsToVolumes](#cfn-fsx-filesystem-openzfsconfiguration-copytagstovolumes): Boolean
  [DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-openzfsconfiguration-dailyautomaticbackupstarttime): String
  [DeploymentType](#cfn-fsx-filesystem-openzfsconfiguration-deploymenttype): String
  [DiskIopsConfiguration](#cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration): 
    DiskIopsConfiguration
  [RootVolumeConfiguration](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration): 
    RootVolumeConfiguration
  [ThroughputCapacity](#cfn-fsx-filesystem-openzfsconfiguration-throughputcapacity): Integer
  [WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-openzfsconfiguration-weeklymaintenancestarttime): String
```

## Properties<a name="aws-properties-fsx-filesystem-openzfsconfiguration-properties"></a>

`AutomaticBackupRetentionDays`  <a name="cfn-fsx-filesystem-openzfsconfiguration-automaticbackupretentiondays"></a>
The number of days to retain automatic backups\. Setting this property to `0` disables automatic backups\. You can retain automatic backups for a maximum of 90 days\. The default is `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTagsToBackups`  <a name="cfn-fsx-filesystem-openzfsconfiguration-copytagstobackups"></a>
A Boolean value indicating whether tags for the file system should be copied to backups\. This value defaults to `false`\. If it's set to `true`, all tags for the file system are copied to all automatic and user\-initiated backups where the user doesn't specify tags\. If this value is `true`, and you specify one or more tags, only the specified tags are copied to backups\. If you specify one or more tags when creating a user\-initiated backup, no tags are copied from the file system, regardless of this value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTagsToVolumes`  <a name="cfn-fsx-filesystem-openzfsconfiguration-copytagstovolumes"></a>
A Boolean value indicating whether tags for the volume should be copied to snapshots\. This value defaults to `false`\. If it's set to `true`, all tags for the volume are copied to snapshots where the user doesn't specify tags\. If this value is `true`, and you specify one or more tags, only the specified tags are copied to snapshots\. If you specify one or more tags when creating the snapshot, no tags are copied from the volume, regardless of this value\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DailyAutomaticBackupStartTime`  <a name="cfn-fsx-filesystem-openzfsconfiguration-dailyautomaticbackupstarttime"></a>
A recurring daily time, in the format `HH:MM`\. `HH` is the zero\-padded hour of the day \(0\-23\), and `MM` is the zero\-padded minute of the hour\. For example, `05:00` specifies 5 AM daily\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentType`  <a name="cfn-fsx-filesystem-openzfsconfiguration-deploymenttype"></a>
Specifies the file system deployment type\. Amazon FSx for OpenZFS supports `SINGLE_AZ_1`\. `SINGLE_AZ_1` deployment type is configured for redundancy within a single Availability Zone\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SINGLE_AZ_1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DiskIopsConfiguration`  <a name="cfn-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration"></a>
The SSD IOPS \(input/output operations per second\) configuration for an Amazon FSx for NetApp ONTAP or Amazon FSx for OpenZFS file system\. The default is 3 IOPS per GB of storage capacity, but you can provision additional IOPS per GB of storage\. The configuration consists of the total number of provisioned SSD IOPS and how the amount was provisioned \(by the customer or by the system\)\.  
*Required*: No  
*Type*: [DiskIopsConfiguration](aws-properties-fsx-filesystem-openzfsconfiguration-diskiopsconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RootVolumeConfiguration`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration"></a>
The configuration Amazon FSx uses when creating the root value of the Amazon FSx for OpenZFS file system\. All volumes are children of the root volume\.   
*Required*: No  
*Type*: [RootVolumeConfiguration](aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThroughputCapacity`  <a name="cfn-fsx-filesystem-openzfsconfiguration-throughputcapacity"></a>
Specifies the throughput of an Amazon FSx for OpenZFS file system, measured in megabytes per second \(MB/s\)\. Valid values are 64, 128, 256, 512, 1024, 2048, 3072, or 4096 MB/s\. You pay for additional throughput capacity that you provision\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `8`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeeklyMaintenanceStartTime`  <a name="cfn-fsx-filesystem-openzfsconfiguration-weeklymaintenancestarttime"></a>
A recurring weekly time, in the format `D:HH:MM`\.   
 `D` is the day of the week, for which 1 represents Monday and 7 represents Sunday\. For further details, see [the ISO\-8601 spec as described on Wikipedia](https://en.wikipedia.org/wiki/ISO_week_date)\.  
 `HH` is the zero\-padded hour of the day \(0\-23\), and `MM` is the zero\-padded minute of the hour\.   
For example, `1:05:00` specifies maintenance at 5 AM Monday\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)