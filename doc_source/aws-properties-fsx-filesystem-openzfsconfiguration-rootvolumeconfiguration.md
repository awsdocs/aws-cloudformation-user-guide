# AWS::FSx::FileSystem RootVolumeConfiguration<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration"></a>

The configuration of an Amazon FSx for OpenZFS root volume\.

## Syntax<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-syntax.json"></a>

```
{
  "[CopyTagsToSnapshots](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-copytagstosnapshots)" : Boolean,
  "[DataCompressionType](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-datacompressiontype)" : String,
  "[NfsExports](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports)" : [ NfsExports, ... ],
  "[ReadOnly](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-readonly)" : Boolean,
  "[RecordSizeKiB](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-recordsizekib)" : Integer,
  "[UserAndGroupQuotas](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-userandgroupquotas)" : [ UserAndGroupQuotas, ... ]
}
```

### YAML<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-syntax.yaml"></a>

```
  [CopyTagsToSnapshots](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-copytagstosnapshots): Boolean
  [DataCompressionType](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-datacompressiontype): String
  [NfsExports](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports): 
    - NfsExports
  [ReadOnly](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-readonly): Boolean
  [RecordSizeKiB](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-recordsizekib): Integer
  [UserAndGroupQuotas](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-userandgroupquotas): 
    - UserAndGroupQuotas
```

## Properties<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-properties"></a>

`CopyTagsToSnapshots`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-copytagstosnapshots"></a>
A Boolean value indicating whether tags for the volume should be copied to snapshots of the volume\. This value defaults to `false`\. If it's set to `true`, all tags for the volume are copied to snapshots where the user doesn't specify tags\. If this value is `true` and you specify one or more tags, only the specified tags are copied to snapshots\. If you specify one or more tags when creating the snapshot, no tags are copied from the volume, regardless of this value\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataCompressionType`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-datacompressiontype"></a>
Specifies the method used to compress the data on the volume\. The compression type is `NONE` by default\.  
+  `NONE` \- Doesn't compress the data on the volume\. `NONE` is the default\.
+  `ZSTD` \- Compresses the data in the volume using the Zstandard \(ZSTD\) compression algorithm\. Compared to LZ4, Z\-Standard provides a better compression ratio to minimize on\-disk storage utilization\.
+  `LZ4` \- Compresses the data in the volume using the LZ4 compression algorithm\. Compared to Z\-Standard, LZ4 is less compute\-intensive and delivers higher write throughput speeds\.
*Required*: No  
*Type*: String  
*Allowed values*: `LZ4 | NONE | ZSTD`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NfsExports`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports"></a>
The configuration object for mounting a file system\.  
*Required*: No  
*Type*: [List](aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports.md) of [NfsExports](aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports.md)  
*Maximum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReadOnly`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-readonly"></a>
A Boolean value indicating whether the volume is read\-only\. Setting this value to `true` can be useful after you have completed changes to a volume and no longer want changes to occur\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecordSizeKiB`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-recordsizekib"></a>
Specifies the record size of an OpenZFS root volume, in kibibytes \(KiB\)\. Valid values are 4, 8, 16, 32, 64, 128, 256, 512, or 1024 KiB\. The default is 128 KiB\. Most workloads should use the default record size\. Database workflows can benefit from a smaller record size, while streaming workflows can benefit from a larger record size\. For additional guidance on setting a custom record size, see [ Tips for maximizing performance](https://docs.aws.amazon.com/fsx/latest/OpenZFSGuide/performance.html#performance-tips-zfs) in the *Amazon FSx for OpenZFS User Guide*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `4`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserAndGroupQuotas`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-userandgroupquotas"></a>
An object specifying how much storage users or groups can use on the volume\.  
*Required*: No  
*Type*: [List](aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-userandgroupquotas.md) of [UserAndGroupQuotas](aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-userandgroupquotas.md)  
*Maximum*: `500`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)