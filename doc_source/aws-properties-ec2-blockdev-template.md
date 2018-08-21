# Amazon Elastic Block Store Block Device Property<a name="aws-properties-ec2-blockdev-template"></a>

The Amazon Elastic Block Store block device type is an embedded property of the [Amazon EC2 Block Device Mapping Property](aws-properties-ec2-blockdev-mapping.md) property\.

## Syntax<a name="w3ab2c21c14d649b5"></a>

### JSON<a name="aws-properties-ec2-blockdev-template-syntax.json"></a>

```
{
   "[DeleteOnTermination](#cfn-ec2-blockdev-template-deleteontermination)" : Boolean,
   "[Encrypted](#cfn-ec2-blockdev-template-encrypted)" : Boolean,
   "[Iops](#cfn-ec2-blockdev-template-iops)" : Number,
   "[SnapshotId](#cfn-ec2-blockdev-template-snapshotid)" : String,
   "[VolumeSize](#cfn-ec2-blockdev-template-volumesize)" : String,
   "[VolumeType](#cfn-ec2-blockdev-template-volumetype)" : String
}
```

### YAML<a name="aws-properties-ec2-blockdev-template-syntax.yaml"></a>

```
[DeleteOnTermination](#cfn-ec2-blockdev-template-deleteontermination): Boolean
[Encrypted](#cfn-ec2-blockdev-template-encrypted): Boolean
[Iops](#cfn-ec2-blockdev-template-iops): Number
[SnapshotId](#cfn-ec2-blockdev-template-snapshotid): String
[VolumeSize](#cfn-ec2-blockdev-template-volumesize): String
[VolumeType](#cfn-ec2-blockdev-template-volumetype): String
```

## Properties<a name="w3ab2c21c14d649b7"></a>

`DeleteOnTermination`  <a name="cfn-ec2-blockdev-template-deleteontermination"></a>
Determines whether to delete the volume on instance termination\. The default value is `true`\.  
*Required*: No  
*Type*: Boolean

`Encrypted`  <a name="cfn-ec2-blockdev-template-encrypted"></a>
Indicates whether the volume is encrypted\. Encrypted Amazon EBS volumes can only be attached to instance types that support Amazon EBS encryption\. Volumes that are created from encrypted snapshots are automatically encrypted\. You cannot create an encrypted volume from an unencrypted snapshot or vice versa\. If your AMI uses encrypted volumes, you can only launch the AMI on supported instance types\. For more information, see [Amazon EBS encryption](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: Boolean

`Iops`  <a name="cfn-ec2-blockdev-template-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. This can be an integer from 100 – 20000\.  
*Required*: Conditional Required when the [volume type](#cfn-ec2-blockdev-template-volumetype) is `io1`; not used with other volume types\.  
*Type*: Number

`SnapshotId`  <a name="cfn-ec2-blockdev-template-snapshotid"></a>
The snapshot ID of the volume to use to create a block device\.  
*Required*: Conditional If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Type*: String

`VolumeSize`  <a name="cfn-ec2-blockdev-template-volumesize"></a>
The volume size, in gibibytes \(GiB\)\. For valid values, see the `Size` parameter for the [CreateVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) action in the *Amazon EC2 API Reference*\.  
*Required*: Conditional If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`VolumeType`  <a name="cfn-ec2-blockdev-template-volumetype"></a>
The volume type\. If you set the type to `io1`, you must also set the `Iops` property\. For valid values, see the `VolumeType` parameter for the [CreateVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: String

## Example<a name="w3ab2c21c14d649b9"></a>

```
{
   "DeviceName":"/dev/sdc",
   "Ebs":{
      "SnapshotId":"snap-xxxxxx",
      "VolumeSize":"50",
      "VolumeType":"io1",
      "Iops":"1000",
      "DeleteOnTermination":"false"
   }
}
```

## See Also<a name="w3ab2c21c14d649c11"></a>
+ [CreateVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) in the *Amazon Elastic Compute Cloud API Reference*