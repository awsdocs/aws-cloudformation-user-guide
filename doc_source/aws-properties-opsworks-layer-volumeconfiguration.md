# AWS::OpsWorks::Layer VolumeConfiguration<a name="aws-properties-opsworks-layer-volumeconfiguration"></a>

Describes an Amazon EBS volume configuration\.

## Syntax<a name="aws-properties-opsworks-layer-volumeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-layer-volumeconfiguration-syntax.json"></a>

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

### YAML<a name="aws-properties-opsworks-layer-volumeconfiguration-syntax.yaml"></a>

```
  [Encrypted](#cfn-opsworks-layer-volumeconfiguration-encrypted): Boolean
  [Iops](#cfn-opsworks-layer-volconfig-iops): Integer
  [MountPoint](#cfn-opsworks-layer-volconfig-mountpoint): String
  [NumberOfDisks](#cfn-opsworks-layer-volconfig-numberofdisks): Integer
  [RaidLevel](#cfn-opsworks-layer-volconfig-raidlevel): Integer
  [Size](#cfn-opsworks-layer-volconfig-size): Integer
  [VolumeType](#cfn-opsworks-layer-volconfig-volumetype): String
```

## Properties<a name="aws-properties-opsworks-layer-volumeconfiguration-properties"></a>

`Encrypted`  <a name="cfn-opsworks-layer-volumeconfiguration-encrypted"></a>
Specifies whether an Amazon EBS volume is encrypted\. For more information, see [Amazon EBS Encryption](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-opsworks-layer-volconfig-iops"></a>
The number of I/O operations per second \(IOPS\) to provision for the volume\. For PIOPS volumes, the IOPS per disk\.  
If you specify `io1` for the volume type, you must specify this property\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MountPoint`  <a name="cfn-opsworks-layer-volconfig-mountpoint"></a>
The volume mount point\. For example "/dev/sdh"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfDisks`  <a name="cfn-opsworks-layer-volconfig-numberofdisks"></a>
The number of disks in the volume\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RaidLevel`  <a name="cfn-opsworks-layer-volconfig-raidlevel"></a>
The volume [RAID level](http://en.wikipedia.org/wiki/Standard_RAID_levels)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-opsworks-layer-volconfig-size"></a>
The volume size\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-opsworks-layer-volconfig-volumetype"></a>
The volume type\. For more information, see [ Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html)\.  
+  `standard` \- Magnetic\. Magnetic volumes must have a minimum size of 1 GiB and a maximum size of 1024 GiB\.
+  `io1` \- Provisioned IOPS \(SSD\)\. PIOPS volumes must have a minimum size of 4 GiB and a maximum size of 16384 GiB\.
+  `gp2` \- General Purpose \(SSD\)\. General purpose volumes must have a minimum size of 1 GiB and a maximum size of 16384 GiB\.
+  `st1` \- Throughput Optimized hard disk drive \(HDD\)\. Throughput optimized HDD volumes must have a minimum size of 500 GiB and a maximum size of 16384 GiB\.
+  `sc1` \- Cold HDD\. Cold HDD volumes must have a minimum size of 500 GiB and a maximum size of 16384 GiB\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)