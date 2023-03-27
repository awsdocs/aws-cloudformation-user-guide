# AWS::FSx::Volume OpenZFSConfiguration<a name="aws-properties-fsx-volume-openzfsconfiguration"></a>

Specifies the configuration of the Amazon FSx for OpenZFS volume that you are creating\.

## Syntax<a name="aws-properties-fsx-volume-openzfsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-volume-openzfsconfiguration-syntax.json"></a>

```
{
  "[CopyTagsToSnapshots](#cfn-fsx-volume-openzfsconfiguration-copytagstosnapshots)" : Boolean,
  "[DataCompressionType](#cfn-fsx-volume-openzfsconfiguration-datacompressiontype)" : String,
  "[NfsExports](#cfn-fsx-volume-openzfsconfiguration-nfsexports)" : [ NfsExports, ... ],
  "[Options](#cfn-fsx-volume-openzfsconfiguration-options)" : [ String, ... ],
  "[OriginSnapshot](#cfn-fsx-volume-openzfsconfiguration-originsnapshot)" : OriginSnapshot,
  "[ParentVolumeId](#cfn-fsx-volume-openzfsconfiguration-parentvolumeid)" : String,
  "[ReadOnly](#cfn-fsx-volume-openzfsconfiguration-readonly)" : Boolean,
  "[RecordSizeKiB](#cfn-fsx-volume-openzfsconfiguration-recordsizekib)" : Integer,
  "[StorageCapacityQuotaGiB](#cfn-fsx-volume-openzfsconfiguration-storagecapacityquotagib)" : Integer,
  "[StorageCapacityReservationGiB](#cfn-fsx-volume-openzfsconfiguration-storagecapacityreservationgib)" : Integer,
  "[UserAndGroupQuotas](#cfn-fsx-volume-openzfsconfiguration-userandgroupquotas)" : [ UserAndGroupQuotas, ... ]
}
```

### YAML<a name="aws-properties-fsx-volume-openzfsconfiguration-syntax.yaml"></a>

```
  [CopyTagsToSnapshots](#cfn-fsx-volume-openzfsconfiguration-copytagstosnapshots): Boolean
  [DataCompressionType](#cfn-fsx-volume-openzfsconfiguration-datacompressiontype): String
  [NfsExports](#cfn-fsx-volume-openzfsconfiguration-nfsexports): 
    - NfsExports
  [Options](#cfn-fsx-volume-openzfsconfiguration-options): 
    - String
  [OriginSnapshot](#cfn-fsx-volume-openzfsconfiguration-originsnapshot): 
    OriginSnapshot
  [ParentVolumeId](#cfn-fsx-volume-openzfsconfiguration-parentvolumeid): String
  [ReadOnly](#cfn-fsx-volume-openzfsconfiguration-readonly): Boolean
  [RecordSizeKiB](#cfn-fsx-volume-openzfsconfiguration-recordsizekib): Integer
  [StorageCapacityQuotaGiB](#cfn-fsx-volume-openzfsconfiguration-storagecapacityquotagib): Integer
  [StorageCapacityReservationGiB](#cfn-fsx-volume-openzfsconfiguration-storagecapacityreservationgib): Integer
  [UserAndGroupQuotas](#cfn-fsx-volume-openzfsconfiguration-userandgroupquotas): 
    - UserAndGroupQuotas
```

## Properties<a name="aws-properties-fsx-volume-openzfsconfiguration-properties"></a>

`CopyTagsToSnapshots`  <a name="cfn-fsx-volume-openzfsconfiguration-copytagstosnapshots"></a>
A Boolean value indicating whether tags for the volume should be copied to snapshots\. This value defaults to `false`\. If it's set to `true`, all tags for the volume are copied to snapshots where the user doesn't specify tags\. If this value is `true`, and you specify one or more tags, only the specified tags are copied to snapshots\. If you specify one or more tags when creating the snapshot, no tags are copied from the volume, regardless of this value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataCompressionType`  <a name="cfn-fsx-volume-openzfsconfiguration-datacompressiontype"></a>
Specifies the method used to compress the data on the volume\. The compression type is `NONE` by default\.  
+  `NONE` \- Doesn't compress the data on the volume\. `NONE` is the default\.
+  `ZSTD` \- Compresses the data in the volume using the Zstandard \(ZSTD\) compression algorithm\. Compared to LZ4, Z\-Standard provides a better compression ratio to minimize on\-disk storage utilization\.
+  `LZ4` \- Compresses the data in the volume using the LZ4 compression algorithm\. Compared to Z\-Standard, LZ4 is less compute\-intensive and delivers higher write throughput speeds\.
*Required*: No  
*Type*: String  
*Allowed values*: `LZ4 | NONE | ZSTD`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NfsExports`  <a name="cfn-fsx-volume-openzfsconfiguration-nfsexports"></a>
The configuration object for mounting a Network File System \(NFS\) file system\.  
*Required*: No  
*Type*: [List](aws-properties-fsx-volume-openzfsconfiguration-nfsexports.md) of [NfsExports](aws-properties-fsx-volume-openzfsconfiguration-nfsexports.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Options`  <a name="cfn-fsx-volume-openzfsconfiguration-options"></a>
To delete the volume's child volumes, snapshots, and clones, use the string `DELETE_CHILD_VOLUMES_AND_SNAPSHOTS`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginSnapshot`  <a name="cfn-fsx-volume-openzfsconfiguration-originsnapshot"></a>
The configuration object that specifies the snapshot to use as the origin of the data for the volume\.  
*Required*: No  
*Type*: [OriginSnapshot](aws-properties-fsx-volume-openzfsconfiguration-originsnapshot.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ParentVolumeId`  <a name="cfn-fsx-volume-openzfsconfiguration-parentvolumeid"></a>
The ID of the volume to use as the parent volume of the volume that you are creating\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `23`  
*Maximum*: `23`  
*Pattern*: `^(fsvol-[0-9a-f]{17,})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReadOnly`  <a name="cfn-fsx-volume-openzfsconfiguration-readonly"></a>
A Boolean value indicating whether the volume is read\-only\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordSizeKiB`  <a name="cfn-fsx-volume-openzfsconfiguration-recordsizekib"></a>
Specifies the suggested block size for a volume in a ZFS dataset, in kibibytes \(KiB\)\. Valid values are 4, 8, 16, 32, 64, 128, 256, 512, or 1024 KiB\. The default is 128 KiB\. We recommend using the default setting for the majority of use cases\. Generally, workloads that write in fixed small or large record sizes may benefit from setting a custom record size, like database workloads \(small record size\) or media streaming workloads \(large record size\)\. For additional guidance on when to set a custom record size, see [ ZFS Record size](https://docs.aws.amazon.com/fsx/latest/OpenZFSGuide/performance.html#record-size-performance) in the *Amazon FSx for OpenZFS User Guide*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `4`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageCapacityQuotaGiB`  <a name="cfn-fsx-volume-openzfsconfiguration-storagecapacityquotagib"></a>
Sets the maximum storage size in gibibytes \(GiB\) for the volume\. You can specify a quota that is larger than the storage on the parent volume\. A volume quota limits the amount of storage that the volume can consume to the configured amount, but does not guarantee the space will be available on the parent volume\. To guarantee quota space, you must also set `StorageCapacityReservationGiB`\. To *not* specify a storage capacity quota, set this to `-1`\.   
For more information, see [Volume properties](https://docs.aws.amazon.com/fsx/latest/OpenZFSGuide/managing-volumes.html#volume-properties) in the *Amazon FSx for OpenZFS User Guide*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `-1`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageCapacityReservationGiB`  <a name="cfn-fsx-volume-openzfsconfiguration-storagecapacityreservationgib"></a>
Specifies the amount of storage in gibibytes \(GiB\) to reserve from the parent volume\. Setting `StorageCapacityReservationGiB` guarantees that the specified amount of storage space on the parent volume will always be available for the volume\. You can't reserve more storage than the parent volume has\. To *not* specify a storage capacity reservation, set this to `0` or `-1`\. For more information, see [Volume properties](https://docs.aws.amazon.com/fsx/latest/OpenZFSGuide/managing-volumes.html#volume-properties) in the *Amazon FSx for OpenZFS User Guide*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `-1`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserAndGroupQuotas`  <a name="cfn-fsx-volume-openzfsconfiguration-userandgroupquotas"></a>
An object specifying how much storage users or groups can use on the volume\.  
*Required*: No  
*Type*: [List](aws-properties-fsx-volume-openzfsconfiguration-userandgroupquotas.md) of [UserAndGroupQuotas](aws-properties-fsx-volume-openzfsconfiguration-userandgroupquotas.md)  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)