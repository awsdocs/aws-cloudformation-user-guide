# AWS::FSx::Volume OntapConfiguration<a name="aws-properties-fsx-volume-ontapconfiguration"></a>

Specifies the configuration of the ONTAP volume that you are creating\.

## Syntax<a name="aws-properties-fsx-volume-ontapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-volume-ontapconfiguration-syntax.json"></a>

```
{
  "[JunctionPath](#cfn-fsx-volume-ontapconfiguration-junctionpath)" : String,
  "[SecurityStyle](#cfn-fsx-volume-ontapconfiguration-securitystyle)" : String,
  "[SizeInMegabytes](#cfn-fsx-volume-ontapconfiguration-sizeinmegabytes)" : String,
  "[StorageEfficiencyEnabled](#cfn-fsx-volume-ontapconfiguration-storageefficiencyenabled)" : String,
  "[StorageVirtualMachineId](#cfn-fsx-volume-ontapconfiguration-storagevirtualmachineid)" : String,
  "[TieringPolicy](#cfn-fsx-volume-ontapconfiguration-tieringpolicy)" : TieringPolicy
}
```

### YAML<a name="aws-properties-fsx-volume-ontapconfiguration-syntax.yaml"></a>

```
  [JunctionPath](#cfn-fsx-volume-ontapconfiguration-junctionpath): String
  [SecurityStyle](#cfn-fsx-volume-ontapconfiguration-securitystyle): String
  [SizeInMegabytes](#cfn-fsx-volume-ontapconfiguration-sizeinmegabytes): String
  [StorageEfficiencyEnabled](#cfn-fsx-volume-ontapconfiguration-storageefficiencyenabled): String
  [StorageVirtualMachineId](#cfn-fsx-volume-ontapconfiguration-storagevirtualmachineid): String
  [TieringPolicy](#cfn-fsx-volume-ontapconfiguration-tieringpolicy): 
    TieringPolicy
```

## Properties<a name="aws-properties-fsx-volume-ontapconfiguration-properties"></a>

`JunctionPath`  <a name="cfn-fsx-volume-ontapconfiguration-junctionpath"></a>
Specifies the location in the SVM's namespace where the volume is mounted\. The `JunctionPath` must have a leading forward slash, such as `/vol3`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,255}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityStyle`  <a name="cfn-fsx-volume-ontapconfiguration-securitystyle"></a>
The security style for the volume\. Specify one of the following values:  
+  `UNIX` if the file system is managed by a UNIX administrator, the majority of users are NFS clients, and an application accessing the data uses a UNIX user as the service account\. `UNIX` is the default\.
+  `NTFS` if the file system is managed by a Windows administrator, the majority of users are SMB clients, and an application accessing the data uses a Windows user as the service account\.
+  `MIXED` if the file system is managed by both UNIX and Windows administrators and users consist of both NFS and SMB clients\.
*Required*: No  
*Type*: String  
*Allowed values*: `MIXED | NTFS | UNIX`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeInMegabytes`  <a name="cfn-fsx-volume-ontapconfiguration-sizeinmegabytes"></a>
Specifies the size of the volume, in megabytes \(MB\), that you are creating\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageEfficiencyEnabled`  <a name="cfn-fsx-volume-ontapconfiguration-storageefficiencyenabled"></a>
Set to true to enable deduplication, compression, and compaction storage efficiency features on the volume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageVirtualMachineId`  <a name="cfn-fsx-volume-ontapconfiguration-storagevirtualmachineid"></a>
Specifies the ONTAP SVM in which to create the volume\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `21`  
*Maximum*: `21`  
*Pattern*: `^(svm-[0-9a-f]{17,})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TieringPolicy`  <a name="cfn-fsx-volume-ontapconfiguration-tieringpolicy"></a>
Describes the data tiering policy for an ONTAP volume\. When enabled, Amazon FSx for ONTAP's intelligent tiering automatically transitions a volume's data between the file system's primary storage and capacity pool storage based on your access patterns\.  
Valid tiering policies are the following:  
+  `SNAPSHOT_ONLY` \- \(Default value\) moves cold snapshots to the capacity pool storage tier\.
+  `AUTO` \- moves cold user data and snapshots to the capacity pool storage tier based on your access patterns\.
+  `ALL` \- moves all user data blocks in both the active file system and Snapshot copies to the storage pool tier\.
+  `NONE` \- keeps a volume's data in the primary storage tier, preventing it from being moved to the capacity pool tier\.
*Required*: No  
*Type*: [TieringPolicy](aws-properties-fsx-volume-ontapconfiguration-tieringpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)