# AWS::AutoScaling::LaunchConfiguration BlockDevice<a name="aws-properties-as-launchconfig-blockdev-template"></a>

 `BlockDevice` is a subproperty of [BlockDeviceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig-blockdev-mapping.html) that describes an Amazon EBS volume\.

## Syntax<a name="aws-properties-as-launchconfig-blockdev-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-launchconfig-blockdev-template-syntax.json"></a>

```
{
  "[DeleteOnTermination](#cfn-as-launchconfig-blockdev-template-deleteonterm)" : Boolean,
  "[Encrypted](#cfn-as-launchconfig-blockdev-template-encrypted)" : Boolean,
  "[Iops](#cfn-as-launchconfig-blockdev-template-iops)" : Integer,
  "[SnapshotId](#cfn-as-launchconfig-blockdev-template-snapshotid)" : String,
  "[Throughput](#cfn-as-launchconfig-blockdev-template-throughput)" : Integer,
  "[VolumeSize](#cfn-as-launchconfig-blockdev-template-volumesize)" : Integer,
  "[VolumeType](#cfn-as-launchconfig-blockdev-template-volumetype)" : String
}
```

### YAML<a name="aws-properties-as-launchconfig-blockdev-template-syntax.yaml"></a>

```
  [DeleteOnTermination](#cfn-as-launchconfig-blockdev-template-deleteonterm): Boolean
  [Encrypted](#cfn-as-launchconfig-blockdev-template-encrypted): Boolean
  [Iops](#cfn-as-launchconfig-blockdev-template-iops): Integer
  [SnapshotId](#cfn-as-launchconfig-blockdev-template-snapshotid): String
  [Throughput](#cfn-as-launchconfig-blockdev-template-throughput): Integer
  [VolumeSize](#cfn-as-launchconfig-blockdev-template-volumesize): Integer
  [VolumeType](#cfn-as-launchconfig-blockdev-template-volumetype): String
```

## Properties<a name="aws-properties-as-launchconfig-blockdev-template-properties"></a>

`DeleteOnTermination`  <a name="cfn-as-launchconfig-blockdev-template-deleteonterm"></a>
Indicates whether the volume is deleted on instance termination\. For Amazon EC2 Auto Scaling, the default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-as-launchconfig-blockdev-template-encrypted"></a>
Specifies whether the volume should be encrypted\. Encrypted EBS volumes can only be attached to instances that support Amazon EBS encryption\. For more information, see [Supported Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#EBSEncryption_supported_instances)\. If your AMI uses encrypted volumes, you can also only launch it on supported instance types\.  
If you are creating a volume from a snapshot, you cannot specify an encryption value\. Volumes that are created from encrypted snapshots are automatically encrypted, and volumes that are created from unencrypted snapshots are automatically unencrypted\. By default, encrypted snapshots use the AWS managed CMK that is used for EBS encryption, but you can specify a custom CMK when you create the snapshot\. The ability to encrypt a snapshot during copying also allows you to apply a new CMK to an already\-encrypted snapshot\. Volumes restored from the resulting copy are only accessible using the new CMK\.  
Enabling [encryption by default](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#encryption-by-default) results in all EBS volumes being encrypted with the AWS managed CMK or a customer managed CMK, whether or not the snapshot was encrypted\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-as-launchconfig-blockdev-template-iops"></a>
The number of input/output \(I/O\) operations per second \(IOPS\) to provision for the volume\. For `gp3` and `io1` volumes, this represents the number of IOPS that are provisioned for the volume\. For `gp2` volumes, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\.   
The following are the supported values for each volume type:   
+  `gp3`: 3,000\-16,000 IOPS
+  `io1`: 100\-64,000 IOPS
For `io1` volumes, we guarantee 64,000 IOPS only for [Instances built on the Nitro System](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\.   
 `Iops` is supported when the volume type is `gp3` or `io1` and required only when the volume type is `io1`\. \(Not used with `standard`, `gp2`, `st1`, or `sc1` volumes\.\)   
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-as-launchconfig-blockdev-template-snapshotid"></a>
The snapshot ID of the volume to use\.  
You must specify either a `VolumeSize` or a `SnapshotId`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Throughput`  <a name="cfn-as-launchconfig-blockdev-template-throughput"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-as-launchconfig-blockdev-template-volumesize"></a>
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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-as-launchconfig-blockdev-template-volumetype"></a>
The volume type\. For more information, see [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
Valid Values: `standard` \| `io1` \| `gp2` \| `st1` \| `sc1` \| `gp3`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-as-launchconfig-blockdev-template--seealso"></a>
+ [Required CMK key policy for use with encrypted volumes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/key-policy-requirements-EBS-encryption.html) in the *Amazon EC2 Auto Scaling User Guide*
+ [Using encryption with EBS\-backed AMIs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIEncryption.html) in the *Amazon EC2 User Guide for Linux Instances*

