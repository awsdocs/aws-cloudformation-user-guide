# AWS OpsWorks Instance BlockDeviceMapping EbsBlockDevice<a name="aws-properties-opsworks-instance-blockdevicemapping-ebsblockdevice"></a>

`EbsBlockDevice` is a property of the [AWS OpsWorks Instance BlockDeviceMapping](aws-properties-opsworks-instance-blockdevicemapping.md) property that defines a block device for an Amazon Elastic Block Store \(Amazon EBS\) volume\.

## Syntax<a name="aws-properties-opsworks-instance-blockdevicemapping-ebsblockdevice-syntax"></a>

### JSON<a name="aws-properties-opsworks-instance-blockdevicemapping-ebsblockdevice-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-deleteontermination)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-iops)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-snapshotid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-volumesize)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-volumetype)" : String
}
```

### YAML<a name="aws-properties-opsworks-instance-blockdevicemapping-ebsblockdevice-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-deleteontermination): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-iops): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-snapshotid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-volumesize): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-blockdevicemapping-ebsblockdevice-volumetype): String
```

## Properties<a name="aws-properties-opsworks-instance-blockdevicemapping-ebsblockdevice-properties"></a>

`DeleteOnTermination`  
Indicates whether to delete the volume when the instance is terminated\.  
*Required: *No  
*Type*: Boolean

`Iops`  
The number of I/O operations per second \(IOPS\) that the volume supports\. For more information, see [Iops](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required: *No  
*Type*: Integer

`SnapshotId`  
The snapshot ID of the volume that you want to use\. If you specify both the `SnapshotId` and `VolumeSize` properties, `VolumeSize` must be equal to or greater than the size of the snapshot\.  
*Required: *No  
*Type*: String

`VolumeSize`  
The volume size, in Gibibytes \(GiB\)\. If you specify both the `SnapshotId` and `VolumeSize` properties, `VolumeSize` must be equal to or greater than the size of the snapshot\. For more information about specifying volume size, see [VolumeSize](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required: *No  
*Type*: Integer

`VolumeType`  
The volume type\. For more information about specifying the volume type, see [VolumeType](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required: *No  
*Type*: String