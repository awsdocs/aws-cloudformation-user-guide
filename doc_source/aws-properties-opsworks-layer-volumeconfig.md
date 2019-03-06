# AWS OpsWorks VolumeConfiguration<a name="aws-properties-opsworks-layer-volumeconfig"></a>

Describes the Amazon EBS volumes for the [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md) resource type\.

## Syntax<a name="w13ab1c21c10d183c29c37b5"></a>

### JSON<a name="aws-properties-opsworks-layer-volumeconfig-syntax.json"></a>

```
{
  "[Encrypted](#cfn-opsworks-layer-volumeconfiguration-encrypted)" : Boolean,
  "[Iops](#cfn-opsworks-layer-volconfig-iops)" : Integer,
  "[MountPoint](#cfn-opsworks-layer-volconfig-mountpoint)" : String,
  "[NumberOfDisks](#cfn-opsworks-layer-volconfig-numberofdisks)" : Integer,
  "[RaidLevel](#cfn-opsworks-layer-volconfig-raidlevel)" : Integer,
  "[Size](#cfn-opsworks-layer-volconfig-size)" : Integer,
  "[VolumeType](#cfn-opsworks-layer-volconfig-volumetype)" : String
}
```

### YAML<a name="aws-properties-opsworks-layer-volumeconfig-syntax.yaml"></a>

```
[Encrypted](#cfn-opsworks-layer-volumeconfiguration-encrypted): Boolean
[Iops](#cfn-opsworks-layer-volconfig-iops): Integer
[MountPoint](#cfn-opsworks-layer-volconfig-mountpoint): String
[NumberOfDisks](#cfn-opsworks-layer-volconfig-numberofdisks): Integer
[RaidLevel](#cfn-opsworks-layer-volconfig-raidlevel): Integer
[Size](#cfn-opsworks-layer-volconfig-size): Integer
[VolumeType](#cfn-opsworks-layer-volconfig-volumetype): String
```

## Properties<a name="w13ab1c21c10d183c29c37b7"></a>

`Encrypted`  <a name="cfn-opsworks-layer-volumeconfiguration-encrypted"></a>
Specifies whether an Amazon EBS volume is encrypted\.   
*Required*: No  
*Type*: Boolean

`Iops`  <a name="cfn-opsworks-layer-volconfig-iops"></a>
The number of I/O operations per second \(IOPS\) to provision for the volume\.  
*Required*: Conditional\. If you specify `io1` for the volume type, you must specify this property\.  
*Type*: Integer

`MountPoint`  <a name="cfn-opsworks-layer-volconfig-mountpoint"></a>
The volume mount point, such as `/dev/sdh`\.  
*Required*: Yes  
*Type*: String

`NumberOfDisks`  <a name="cfn-opsworks-layer-volconfig-numberofdisks"></a>
The number of disks in the volume\.  
*Required*: Yes  
*Type*: Integer

`RaidLevel`  <a name="cfn-opsworks-layer-volconfig-raidlevel"></a>
The volume RAID level\.  
*Required*: No  
*Type*: Integer

`Size`  <a name="cfn-opsworks-layer-volconfig-size"></a>
The volume size\.  
*Required*: Yes  
*Type*: Integer

`VolumeType`  <a name="cfn-opsworks-layer-volconfig-volumetype"></a>
The type of volume, such as magnetic or SSD\. For valid values, see [VolumeConfiguration](https://docs.aws.amazon.com/opsworks/latest/APIReference/API_VolumeConfiguration.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: No  
*Type*: String