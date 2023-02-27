# AWS::FSx::FileSystem WindowsConfiguration<a name="aws-properties-fsx-filesystem-windowsconfiguration"></a>

The Microsoft Windows configuration for the file system that's being created\. 

## Syntax<a name="aws-properties-fsx-filesystem-windowsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-windowsconfiguration-syntax.json"></a>

```
{
  "[ActiveDirectoryId](#cfn-fsx-filesystem-windowsconfiguration-activedirectoryid)" : String,
  "[Aliases](#cfn-fsx-filesystem-windowsconfiguration-aliases)" : [ String, ... ],
  "[AuditLogConfiguration](#cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration)" : AuditLogConfiguration,
  "[AutomaticBackupRetentionDays](#cfn-fsx-filesystem-windowsconfiguration-automaticbackupretentiondays)" : Integer,
  "[CopyTagsToBackups](#cfn-fsx-filesystem-windowsconfiguration-copytagstobackups)" : Boolean,
  "[DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-windowsconfiguration-dailyautomaticbackupstarttime)" : String,
  "[DeploymentType](#cfn-fsx-filesystem-windowsconfiguration-deploymenttype)" : String,
  "[PreferredSubnetId](#cfn-fsx-filesystem-windowsconfiguration-preferredsubnetid)" : String,
  "[SelfManagedActiveDirectoryConfiguration](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration)" : SelfManagedActiveDirectoryConfiguration,
  "[ThroughputCapacity](#cfn-fsx-filesystem-windowsconfiguration-throughputcapacity)" : Integer,
  "[WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-windowsconfiguration-weeklymaintenancestarttime)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-windowsconfiguration-syntax.yaml"></a>

```
  [ActiveDirectoryId](#cfn-fsx-filesystem-windowsconfiguration-activedirectoryid): String
  [Aliases](#cfn-fsx-filesystem-windowsconfiguration-aliases): 
    - String
  [AuditLogConfiguration](#cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration): 
    AuditLogConfiguration
  [AutomaticBackupRetentionDays](#cfn-fsx-filesystem-windowsconfiguration-automaticbackupretentiondays): Integer
  [CopyTagsToBackups](#cfn-fsx-filesystem-windowsconfiguration-copytagstobackups): Boolean
  [DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-windowsconfiguration-dailyautomaticbackupstarttime): String
  [DeploymentType](#cfn-fsx-filesystem-windowsconfiguration-deploymenttype): String
  [PreferredSubnetId](#cfn-fsx-filesystem-windowsconfiguration-preferredsubnetid): String
  [SelfManagedActiveDirectoryConfiguration](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration): 
    SelfManagedActiveDirectoryConfiguration
  [ThroughputCapacity](#cfn-fsx-filesystem-windowsconfiguration-throughputcapacity): Integer
  [WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-windowsconfiguration-weeklymaintenancestarttime): String
```

## Properties<a name="aws-properties-fsx-filesystem-windowsconfiguration-properties"></a>

`ActiveDirectoryId`  <a name="cfn-fsx-filesystem-windowsconfiguration-activedirectoryid"></a>
The ID for an existing AWS Managed Microsoft Active Directory \(AD\) instance that the file system should join when it's created\. Required if you are joining the file system to an existing AWS Managed Microsoft AD\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `^d-[0-9a-f]{10}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Aliases`  <a name="cfn-fsx-filesystem-windowsconfiguration-aliases"></a>
An array of one or more DNS alias names that you want to associate with the Amazon FSx file system\. Aliases allow you to use existing DNS names to access the data in your Amazon FSx file system\. You can associate up to 50 aliases with a file system at any time\.   
For more information, see [Working with DNS Aliases](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/managing-dns-aliases.html) and [Walkthrough 5: Using DNS aliases to access your file system](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/walkthrough05-file-system-custom-CNAME.html), including additional steps you must take to be able to access your file system using a DNS alias\.  
An alias name has to meet the following requirements:  
+ Formatted as a fully\-qualified domain name \(FQDN\), `hostname.domain`, for example, `accounting.example.com`\.
+ Can contain alphanumeric characters, the underscore \(\_\), and the hyphen \(\-\)\.
+ Cannot start or end with a hyphen\.
+ Can start with a numeric\.
For DNS alias names, Amazon FSx stores alphabetical characters as lowercase letters \(a\-z\), regardless of how you specify them: as uppercase letters, lowercase letters, or the corresponding letters in escape codes\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuditLogConfiguration`  <a name="cfn-fsx-filesystem-windowsconfiguration-auditlogconfiguration"></a>
The configuration that Amazon FSx for Windows File Server uses to audit and log user accesses of files, folders, and file shares on the Amazon FSx for Windows File Server file system\.  
*Required*: No  
*Type*: [AuditLogConfiguration](aws-properties-fsx-filesystem-windowsconfiguration-auditlogconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutomaticBackupRetentionDays`  <a name="cfn-fsx-filesystem-windowsconfiguration-automaticbackupretentiondays"></a>
The number of days to retain automatic backups\. Setting this property to `0` disables automatic backups\. You can retain automatic backups for a maximum of 90 days\. The default is `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CopyTagsToBackups`  <a name="cfn-fsx-filesystem-windowsconfiguration-copytagstobackups"></a>
A boolean flag indicating whether tags for the file system should be copied to backups\. This value defaults to false\. If it's set to true, all tags for the file system are copied to all automatic and user\-initiated backups where the user doesn't specify tags\. If this value is true, and you specify one or more tags, only the specified tags are copied to backups\. If you specify one or more tags when creating a user\-initiated backup, no tags are copied from the file system, regardless of this value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DailyAutomaticBackupStartTime`  <a name="cfn-fsx-filesystem-windowsconfiguration-dailyautomaticbackupstarttime"></a>
A recurring daily time, in the format `HH:MM`\. `HH` is the zero\-padded hour of the day \(0\-23\), and `MM` is the zero\-padded minute of the hour\. For example, `05:00` specifies 5 AM daily\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentType`  <a name="cfn-fsx-filesystem-windowsconfiguration-deploymenttype"></a>
Specifies the file system deployment type, valid values are the following:  
+  `MULTI_AZ_1` \- Deploys a high availability file system that is configured for Multi\-AZ redundancy to tolerate temporary Availability Zone \(AZ\) unavailability\. You can only deploy a Multi\-AZ file system in AWS Regions that have a minimum of three Availability Zones\. Also supports HDD storage type
+  `SINGLE_AZ_1` \- \(Default\) Choose to deploy a file system that is configured for single AZ redundancy\.
+  `SINGLE_AZ_2` \- The latest generation Single AZ file system\. Specifies a file system that is configured for single AZ redundancy and supports HDD storage type\.
For more information, see [ Availability and Durability: Single\-AZ and Multi\-AZ File Systems](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `MULTI_AZ_1 | SINGLE_AZ_1 | SINGLE_AZ_2`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreferredSubnetId`  <a name="cfn-fsx-filesystem-windowsconfiguration-preferredsubnetid"></a>
Required when `DeploymentType` is set to `MULTI_AZ_1`\. This specifies the subnet in which you want the preferred file server to be located\. For in\-AWS applications, we recommend that you launch your clients in the same availability zone as your preferred file server to reduce cross\-availability zone data transfer costs and minimize latency\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SelfManagedActiveDirectoryConfiguration`  <a name="cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration"></a>
The configuration that Amazon FSx uses to join a FSx for Windows File Server file system or an ONTAP storage virtual machine \(SVM\) to a self\-managed \(including on\-premises\) Microsoft Active Directory \(AD\) directory\. For more information, see [ Using Amazon FSx with your self\-managed Microsoft Active Directory](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/self-managed-AD.html) or [Managing SVMs](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/managing-svms.html)\.  
*Required*: No  
*Type*: [SelfManagedActiveDirectoryConfiguration](aws-properties-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThroughputCapacity`  <a name="cfn-fsx-filesystem-windowsconfiguration-throughputcapacity"></a>
Sets the throughput capacity of an Amazon FSx file system, measured in megabytes per second \(MB/s\), in 2 to the *n*th increments, between 2^3 \(8\) and 2^11 \(2048\)\.  
*Required*: Conditional  
*Type*: Integer  
*Minimum*: `8`  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeeklyMaintenanceStartTime`  <a name="cfn-fsx-filesystem-windowsconfiguration-weeklymaintenancestarttime"></a>
A recurring weekly time, in the format `D:HH:MM`\.   
 `D` is the day of the week, for which 1 represents Monday and 7 represents Sunday\. For further details, see [the ISO\-8601 spec as described on Wikipedia](https://en.wikipedia.org/wiki/ISO_week_date)\.  
 `HH` is the zero\-padded hour of the day \(0\-23\), and `MM` is the zero\-padded minute of the hour\.   
For example, `1:05:00` specifies maintenance at 5 AM Monday\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)