# AWS::AutoScaling::LaunchConfiguration BlockDevice<a name="aws-properties-autoscaling-launchconfiguration-blockdevice"></a>

 `BlockDevice` is a property of the `EBS` property of the [AWS::AutoScaling::LaunchConfiguration BlockDeviceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig-blockdev-mapping.html) property type that describes an Amazon EBS volume\.

## Syntax<a name="aws-properties-autoscaling-launchconfiguration-blockdevice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-launchconfiguration-blockdevice-syntax.json"></a>

```
{
  "[DeleteOnTermination](#cfn-autoscaling-launchconfiguration-blockdevice-deleteontermination)" : Boolean,
  "[Encrypted](#cfn-autoscaling-launchconfiguration-blockdevice-encrypted)" : Boolean,
  "[Iops](#cfn-autoscaling-launchconfiguration-blockdevice-iops)" : Integer,
  "[SnapshotId](#cfn-autoscaling-launchconfiguration-blockdevice-snapshotid)" : String,
  "[Throughput](#cfn-autoscaling-launchconfiguration-blockdevice-throughput)" : Integer,
  "[VolumeSize](#cfn-autoscaling-launchconfiguration-blockdevice-volumesize)" : Integer,
  "[VolumeType](#cfn-autoscaling-launchconfiguration-blockdevice-volumetype)" : String
}
```

### YAML<a name="aws-properties-autoscaling-launchconfiguration-blockdevice-syntax.yaml"></a>

```
  [DeleteOnTermination](#cfn-autoscaling-launchconfiguration-blockdevice-deleteontermination): Boolean
  [Encrypted](#cfn-autoscaling-launchconfiguration-blockdevice-encrypted): Boolean
  [Iops](#cfn-autoscaling-launchconfiguration-blockdevice-iops): Integer
  [SnapshotId](#cfn-autoscaling-launchconfiguration-blockdevice-snapshotid): String
  [Throughput](#cfn-autoscaling-launchconfiguration-blockdevice-throughput): Integer
  [VolumeSize](#cfn-autoscaling-launchconfiguration-blockdevice-volumesize): Integer
  [VolumeType](#cfn-autoscaling-launchconfiguration-blockdevice-volumetype): String
```

## Properties<a name="aws-properties-autoscaling-launchconfiguration-blockdevice-properties"></a>

`DeleteOnTermination`  <a name="cfn-autoscaling-launchconfiguration-blockdevice-deleteontermination"></a>
Indicates whether the volume is deleted on instance termination\. For Amazon EC2 Auto Scaling, the default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Encrypted`  <a name="cfn-autoscaling-launchconfiguration-blockdevice-encrypted"></a>
Specifies whether the volume should be encrypted\. Encrypted EBS volumes can only be attached to instances that support Amazon EBS encryption\. For more information, see [Supported instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#EBSEncryption_supported_instances)\. If your AMI uses encrypted volumes, you can also only launch it on supported instance types\.  
If you are creating a volume from a snapshot, you cannot create an unencrypted volume from an encrypted snapshot\. Also, you cannot specify a KMS key ID when using a launch configuration\.  
If you enable encryption by default, the EBS volumes that you create are always encrypted, either using the AWS managed KMS key or a customer\-managed KMS key, regardless of whether the snapshot was encrypted\.   
For more information, see [Use AWS KMS keys to encrypt Amazon EBS volumes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-data-protection.html#encryption) in the *Amazon EC2 Auto Scaling User Guide*\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Iops`  <a name="cfn-autoscaling-launchconfiguration-blockdevice-iops"></a>
The number of input/output \(I/O\) operations per second \(IOPS\) to provision for the volume\. For `gp3` and `io1` volumes, this represents the number of IOPS that are provisioned for the volume\. For `gp2` volumes, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\.   
The following are the supported values for each volume type:   
+  `gp3`: 3,000\-16,000 IOPS
+  `io1`: 100\-64,000 IOPS
For `io1` volumes, we guarantee 64,000 IOPS only for [Instances built on the Nitro System](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\.   
 `Iops` is supported when the volume type is `gp3` or `io1` and required only when the volume type is `io1`\. \(Not used with `standard`, `gp2`, `st1`, or `sc1` volumes\.\)   
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotId`  <a name="cfn-autoscaling-launchconfiguration-blockdevice-snapshotid"></a>
The snapshot ID of the volume to use\.  
You must specify either a `VolumeSize` or a `SnapshotId`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Throughput`  <a name="cfn-autoscaling-launchconfiguration-blockdevice-throughput"></a>
The throughput \(MiBps\) to provision for a `gp3` volume\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `125`  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeSize`  <a name="cfn-autoscaling-launchconfiguration-blockdevice-volumesize"></a>
The volume size, in GiBs\. The following are the supported volumes sizes for each volume type:   
+  `gp2` and `gp3`: 1\-16,384
+  `io1`: 4\-16,384
+  `st1` and `sc1`: 125\-16,384
+  `standard`: 1\-1,024
You must specify either a `SnapshotId` or a `VolumeSize`\. If you specify both `SnapshotId` and `VolumeSize`, the volume size must be equal or greater than the size of the snapshot\.  
*Required*: Conditional  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `16384`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeType`  <a name="cfn-autoscaling-launchconfiguration-blockdevice-volumetype"></a>
The volume type\. For more information, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
Valid values: `standard` \| `io1` \| `gp2` \| `st1` \| `sc1` \| `gp3`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-autoscaling-launchconfiguration-blockdevice--seealso"></a>
+ [Required KMS key policy for use with encrypted volumes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/key-policy-requirements-EBS-encryption.html) in the *Amazon EC2 Auto Scaling User Guide*
+ [Use encryption with EBS\-backed AMIs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIEncryption.html) in the *Amazon EC2 User Guide for Linux Instances*

