# AWS::FSx::FileSystem LustreConfiguration<a name="aws-properties-fsx-filesystem-lustreconfiguration"></a>

The configuration for the Amazon FSx for Lustre file system\.

## Syntax<a name="aws-properties-fsx-filesystem-lustreconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-lustreconfiguration-syntax.json"></a>

```
{
  "[AutoImportPolicy](#cfn-fsx-filesystem-lustreconfiguration-autoimportpolicy)" : String,
  "[AutomaticBackupRetentionDays](#cfn-fsx-filesystem-lustreconfiguration-automaticbackupretentiondays)" : Integer,
  "[CopyTagsToBackups](#cfn-fsx-filesystem-lustreconfiguration-copytagstobackups)" : Boolean,
  "[DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-lustreconfiguration-dailyautomaticbackupstarttime)" : String,
  "[DeploymentType](#cfn-fsx-filesystem-lustreconfiguration-deploymenttype)" : String,
  "[DriveCacheType](#cfn-fsx-filesystem-lustreconfiguration-drivecachetype)" : String,
  "[ExportPath](#cfn-fsx-filesystem-lustreconfiguration-exportpath)" : String,
  "[ImportedFileChunkSize](#cfn-fsx-filesystem-lustreconfiguration-importedfilechunksize)" : Integer,
  "[ImportPath](#cfn-fsx-filesystem-lustreconfiguration-importpath)" : String,
  "[PerUnitStorageThroughput](#cfn-fsx-filesystem-lustreconfiguration-perunitstoragethroughput)" : Integer,
  "[WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-lustreconfiguration-weeklymaintenancestarttime)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-lustreconfiguration-syntax.yaml"></a>

```
  [AutoImportPolicy](#cfn-fsx-filesystem-lustreconfiguration-autoimportpolicy): String
  [AutomaticBackupRetentionDays](#cfn-fsx-filesystem-lustreconfiguration-automaticbackupretentiondays): Integer
  [CopyTagsToBackups](#cfn-fsx-filesystem-lustreconfiguration-copytagstobackups): Boolean
  [DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-lustreconfiguration-dailyautomaticbackupstarttime): String
  [DeploymentType](#cfn-fsx-filesystem-lustreconfiguration-deploymenttype): String
  [DriveCacheType](#cfn-fsx-filesystem-lustreconfiguration-drivecachetype): String
  [ExportPath](#cfn-fsx-filesystem-lustreconfiguration-exportpath): String
  [ImportedFileChunkSize](#cfn-fsx-filesystem-lustreconfiguration-importedfilechunksize): Integer
  [ImportPath](#cfn-fsx-filesystem-lustreconfiguration-importpath): String
  [PerUnitStorageThroughput](#cfn-fsx-filesystem-lustreconfiguration-perunitstoragethroughput): Integer
  [WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-lustreconfiguration-weeklymaintenancestarttime): String
```

## Properties<a name="aws-properties-fsx-filesystem-lustreconfiguration-properties"></a>

`AutoImportPolicy`  <a name="cfn-fsx-filesystem-lustreconfiguration-autoimportpolicy"></a>
 \(Optional\) When you create your file system, your existing S3 objects appear as file and directory listings\. Use this property to choose how Amazon FSx keeps your file and directory listings up to date as you add or modify objects in your linked S3 bucket\. `AutoImportPolicy` can have the following values:  
+  `NONE` \- \(Default\) AutoImport is off\. Amazon FSx only updates file and directory listings from the linked S3 bucket when the file system is created\. FSx does not update file and directory listings for any new or changed objects after choosing this option\.
+  `NEW` \- AutoImport is on\. Amazon FSx automatically imports directory listings of any new objects added to the linked S3 bucket that do not currently exist in the FSx file system\. 
+  `NEW_CHANGED` \- AutoImport is on\. Amazon FSx automatically imports file and directory listings of any new objects added to the S3 bucket and any existing objects that are changed in the S3 bucket after you choose this option\. 
For more information, see [Automatically import updates from your S3 bucket](https://docs.aws.amazon.com/fsx/latest/LustreGuide/autoimport-data-repo.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NEW | NEW_CHANGED | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutomaticBackupRetentionDays`  <a name="cfn-fsx-filesystem-lustreconfiguration-automaticbackupretentiondays"></a>
The number of days to retain automatic backups\. Setting this to 0 disables automatic backups\. You can retain automatic backups for a maximum of 90 days\. The default is 0\. Only valid for use with `PERSISTENT_1` deployment types\. For more information, see [Working with backups](https://docs.aws.amazon.com/fsx/latest/LustreGuide/using-backups-fsx.html) in the *Amazon FSx for Lustre User Guide*\. \(Default = 0\)  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `90`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTagsToBackups`  <a name="cfn-fsx-filesystem-lustreconfiguration-copytagstobackups"></a>
A boolean flag indicating whether tags for the file system should be copied to backups\. This value defaults to false\. If it's set to true, all tags for the file system are copied to all automatic and user\-initiated backups where the user doesn't specify tags\. If this value is true, and you specify one or more tags, only the specified tags are copied to backups\. If you specify one or more tags when creating a user\-initiated backup, no tags are copied from the file system, regardless of this value\. Only valid for use with `PERSISTENT_1` deployment types\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DailyAutomaticBackupStartTime`  <a name="cfn-fsx-filesystem-lustreconfiguration-dailyautomaticbackupstarttime"></a>
A recurring daily time, in the format` HH:MM`\. `HH` is the zero\-padded hour of the day \(0\-23\), and `MM` is the zero\-padded minute of the hour\. For example, `05:00` specifies 5 AM daily\. Only valid for use with `PERSISTENT_1` deployment types\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentType`  <a name="cfn-fsx-filesystem-lustreconfiguration-deploymenttype"></a>
 Choose `SCRATCH_1` and `SCRATCH_2` deployment types when you need temporary storage and shorter\-term processing of data\. The `SCRATCH_2` deployment type provides in\-transit encryption of data and higher burst throughput capacity than `SCRATCH_1`\.  
Choose `PERSISTENT_1` deployment type for longer\-term storage and workloads and encryption of data in transit\. To learn more about deployment types, see [ FSx for Lustre Deployment Options](https://docs.aws.amazon.com/fsx/latest/LustreGuide/lustre-deployment-types.html)\.  
Encryption of data in\-transit is automatically enabled when you access a `SCRATCH_2` or `PERSISTENT_1` file system from Amazon EC2 instances that [support this feature](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/data-                 protection.html)\. \(Default = `SCRATCH_1`\)   
Encryption of data in\-transit for `SCRATCH_2` and `PERSISTENT_1` deployment types is supported when accessed from supported instance types in supported AWS Regions\. To learn more, [Encrypting Data in Transit](https://docs.aws.amazon.com/fsx/latest/LustreGuide/encryption-in-transit-fsxl.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PERSISTENT_1 | SCRATCH_1 | SCRATCH_2`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DriveCacheType`  <a name="cfn-fsx-filesystem-lustreconfiguration-drivecachetype"></a>
The type of drive cache used by PERSISTENT\_1 file systems that are provisioned with HDD storage devices\. This parameter is required when storage type is HDD\. Set to `READ`, improve the performance for frequently accessed files and allows 20% of the total storage capacity of the file system to be cached\.   
This parameter is required when `StorageType` is set to HDD\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | READ`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExportPath`  <a name="cfn-fsx-filesystem-lustreconfiguration-exportpath"></a>
\(Optional\) The path in Amazon S3 where the root of your Amazon FSx file system is exported\. The path must use the same Amazon S3 bucket as specified in ImportPath\. You can provide an optional prefix to which new and changed data is to be exported from your Amazon FSx for Lustre file system\. If an `ExportPath` value is not provided, Amazon FSx sets a default export path, `s3://import-bucket/FSxLustre[creation-timestamp]`\. The timestamp is in UTC format, for example `s3://import-bucket/FSxLustre20181105T222312Z`\.  
The Amazon S3 export bucket must be the same as the import bucket specified by `ImportPath`\. If you only specify a bucket name, such as `s3://import-bucket`, you get a 1:1 mapping of file system objects to S3 bucket objects\. This mapping means that the input data in S3 is overwritten on export\. If you provide a custom prefix in the export path, such as `s3://import-bucket/[custom-optional-prefix]`, Amazon FSx exports the contents of your file system to that export prefix in the Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `4357`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{3,4357}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImportedFileChunkSize`  <a name="cfn-fsx-filesystem-lustreconfiguration-importedfilechunksize"></a>
\(Optional\) For files imported from a data repository, this value determines the stripe count and maximum amount of data per file \(in MiB\) stored on a single physical disk\. The maximum number of disks that a single file can be striped across is limited by the total number of disks that make up the file system\.  
The default chunk size is 1,024 MiB \(1 GiB\) and can go as high as 512,000 MiB \(500 GiB\)\. Amazon S3 objects have a maximum size of 5 TB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `512000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImportPath`  <a name="cfn-fsx-filesystem-lustreconfiguration-importpath"></a>
\(Optional\) The path to the Amazon S3 bucket \(including the optional prefix\) that you're using as the data repository for your Amazon FSx for Lustre file system\. The root of your FSx for Lustre file system will be mapped to the root of the Amazon S3 bucket you select\. An example is `s3://import-bucket/optional-prefix`\. If you specify a prefix after the Amazon S3 bucket name, only object keys with that prefix are loaded into the file system\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `4357`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{3,4357}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PerUnitStorageThroughput`  <a name="cfn-fsx-filesystem-lustreconfiguration-perunitstoragethroughput"></a>
 Required for the `PERSISTENT_1` deployment type, describes the amount of read and write throughput for each 1 tebibyte of storage, in MB/s/TiB\. File system throughput capacity is calculated by multiplying ﬁle system storage capacity \(TiB\) by the PerUnitStorageThroughput \(MB/s/TiB\)\. For a 2\.4 TiB ﬁle system, provisioning 50 MB/s/TiB of PerUnitStorageThroughput yields 120 MB/s of ﬁle system throughput\. You pay for the amount of throughput that you provision\.   
Valid values for SSD storage: 50, 100, 200\. Valid values for HDD storage: 12, 40\.  
*Required*: Conditional  
*Type*: Integer  
*Minimum*: `12`  
*Maximum*: `200`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WeeklyMaintenanceStartTime`  <a name="cfn-fsx-filesystem-lustreconfiguration-weeklymaintenancestarttime"></a>
\(Optional\) The preferred start time to perform weekly maintenance, formatted d:HH:MM in the UTC time zone, where d is the weekday number, from 1 through 7, beginning with Monday and ending with Sunday\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)