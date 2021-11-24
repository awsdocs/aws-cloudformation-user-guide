# AWS::FSx::FileSystem OntapConfiguration<a name="aws-properties-fsx-filesystem-ontapconfiguration"></a>

Configuration for the FSx for NetApp ONTAP file system\.

## Syntax<a name="aws-properties-fsx-filesystem-ontapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-ontapconfiguration-syntax.json"></a>

```
{
  "[AutomaticBackupRetentionDays](#cfn-fsx-filesystem-ontapconfiguration-automaticbackupretentiondays)" : Integer,
  "[DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-ontapconfiguration-dailyautomaticbackupstarttime)" : String,
  "[DeploymentType](#cfn-fsx-filesystem-ontapconfiguration-deploymenttype)" : String,
  "[DiskIopsConfiguration](#cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration)" : DiskIopsConfiguration,
  "[EndpointIpAddressRange](#cfn-fsx-filesystem-ontapconfiguration-endpointipaddressrange)" : String,
  "[FsxAdminPassword](#cfn-fsx-filesystem-ontapconfiguration-fsxadminpassword)" : String,
  "[PreferredSubnetId](#cfn-fsx-filesystem-ontapconfiguration-preferredsubnetid)" : String,
  "[RouteTableIds](#cfn-fsx-filesystem-ontapconfiguration-routetableids)" : [ String, ... ],
  "[ThroughputCapacity](#cfn-fsx-filesystem-ontapconfiguration-throughputcapacity)" : Integer,
  "[WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-ontapconfiguration-weeklymaintenancestarttime)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-ontapconfiguration-syntax.yaml"></a>

```
  [AutomaticBackupRetentionDays](#cfn-fsx-filesystem-ontapconfiguration-automaticbackupretentiondays): Integer
  [DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-ontapconfiguration-dailyautomaticbackupstarttime): String
  [DeploymentType](#cfn-fsx-filesystem-ontapconfiguration-deploymenttype): String
  [DiskIopsConfiguration](#cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration): 
    DiskIopsConfiguration
  [EndpointIpAddressRange](#cfn-fsx-filesystem-ontapconfiguration-endpointipaddressrange): String
  [FsxAdminPassword](#cfn-fsx-filesystem-ontapconfiguration-fsxadminpassword): String
  [PreferredSubnetId](#cfn-fsx-filesystem-ontapconfiguration-preferredsubnetid): String
  [RouteTableIds](#cfn-fsx-filesystem-ontapconfiguration-routetableids): 
    - String
  [ThroughputCapacity](#cfn-fsx-filesystem-ontapconfiguration-throughputcapacity): Integer
  [WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-ontapconfiguration-weeklymaintenancestarttime): String
```

## Properties<a name="aws-properties-fsx-filesystem-ontapconfiguration-properties"></a>

`AutomaticBackupRetentionDays`  <a name="cfn-fsx-filesystem-ontapconfiguration-automaticbackupretentiondays"></a>
The number of days to retain automatic backups\. Setting this to 0 disables automatic backups\. You can retain automatic backups for a maximum of 90 days\. The default is 0\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DailyAutomaticBackupStartTime`  <a name="cfn-fsx-filesystem-ontapconfiguration-dailyautomaticbackupstarttime"></a>
A recurring daily time, in the format `HH:MM`\. `HH` is the zero\-padded hour of the day \(0\-23\), and `MM` is the zero\-padded minute of the hour\. For example, `05:00` specifies 5 AM daily\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentType`  <a name="cfn-fsx-filesystem-ontapconfiguration-deploymenttype"></a>
Specifies the FSx for ONTAP file system deployment type to use in creating the file system\. `MULTI_AZ_1` is the supported ONTAP deployment type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DiskIopsConfiguration`  <a name="cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration"></a>
The SSD IOPS configuration for the FSx for ONTAP file system\.  
*Required*: No  
*Type*: [DiskIopsConfiguration](aws-properties-fsx-filesystem-ontapconfiguration-diskiopsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointIpAddressRange`  <a name="cfn-fsx-filesystem-ontapconfiguration-endpointipaddressrange"></a>
Specifies the IP address range in which the endpoints to access your file system will be created\. By default, Amazon FSx selects an unused IP address range for you from the 198\.19\.\* range\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FsxAdminPassword`  <a name="cfn-fsx-filesystem-ontapconfiguration-fsxadminpassword"></a>
The ONTAP administrative password for the `fsxadmin` user with which you administer your file system using the NetApp ONTAP CLI and REST API\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredSubnetId`  <a name="cfn-fsx-filesystem-ontapconfiguration-preferredsubnetid"></a>
Required when `DeploymentType` is set to `MULTI_AZ_1`\. This specifies the subnet in which you want the preferred file server to be located\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteTableIds`  <a name="cfn-fsx-filesystem-ontapconfiguration-routetableids"></a>
Specifies the VPC route tables in which your file system's endpoints will be created\. You should specify all VPC route tables associated with the subnets in which your clients are located\. By default, Amazon FSx selects your VPC's default route table\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ThroughputCapacity`  <a name="cfn-fsx-filesystem-ontapconfiguration-throughputcapacity"></a>
Sets the throughput capacity for the FSx for ONTAP file system that you're creating\. Valid values are 512, 1024, and 2048 MBps\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WeeklyMaintenanceStartTime`  <a name="cfn-fsx-filesystem-ontapconfiguration-weeklymaintenancestarttime"></a>
A recurring weekly time, in the format `D:HH:MM`\.  
`D` is the day of the week, for which 1 represents Monday and 7 represents Sunday\. For further details, see [the ISO\-8601 spec as described on Wikipedia](https://en.wikipedia.org/wiki/ISO_week_date)\.  
`HH` is the zero\-padded hour of the day \(0\-23\), and `MM` is the zero\-padded minute of the hour\.  
For example, `1:05:00` specifies maintenance at 5 AM Monday\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)