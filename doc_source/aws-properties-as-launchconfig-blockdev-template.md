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
  [VolumeSize](#cfn-as-launchconfig-blockdev-template-volumesize): Integer
  [VolumeType](#cfn-as-launchconfig-blockdev-template-volumetype): String
```

## Properties<a name="aws-properties-as-launchconfig-blockdev-template-properties"></a>

`DeleteOnTermination`  <a name="cfn-as-launchconfig-blockdev-template-deleteonterm"></a>
Indicates whether to delete the volume when the instance is terminated\. For Amazon EC2 Auto Scaling, the default value is `true`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-as-launchconfig-blockdev-template-encrypted"></a>
Specifies whether the EBS volume is encrypted\. Encrypted EBS volumes can only be attached to instances that support Amazon EBS encryption\. For more information, see [Supported instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#EBSEncryption_supported_instances)\. If your AMI uses encrypted volumes, you can also only launch it on supported instance types\.  
If you are creating a volume from a snapshot, you cannot specify an encryption value\. Volumes that are created from encrypted snapshots are automatically encrypted, and volumes that are created from unencrypted snapshots are automatically unencrypted\. By default, encrypted snapshots use the AWS managed CMK that is used for EBS encryption, but you can specify a custom CMK when you create the snapshot\. The ability to encrypt a snapshot during copying also allows you to apply a new CMK to an already\-encrypted snapshot\. Volumes restored from the resulting copy are only accessible using the new CMK\.   
Enabling [encryption by default](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#encryption-by-default) results in all EBS volumes being encrypted with the AWS managed CMK or a customer managed CMK, whether or not the snapshot was encrypted\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-as-launchconfig-blockdev-template-iops"></a>
The number of I/O operations per second \(IOPS\) to provision for the volume\. The maximum ratio of IOPS to volume size \(in GiB\) is 50:1, so for 5,000 provisioned IOPS, you need at least 100 GiB storage on the volume\. For more information, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
If the volume type is `io1`, this property is required\. \(Not used with `standard`, `gp2`, `st1`, or `sc1` volumes\.\)   
*Required*: Conditional  
*Type*: Integer  
*Minimum*: `100`  
*Maximum*: `20000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-as-launchconfig-blockdev-template-snapshotid"></a>
The snapshot ID of the volume to use\.   
You must specify either a `VolumeSize` or a `SnapshotId`\.   
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-as-launchconfig-blockdev-template-volumesize"></a>
The volume size, in Gibibytes \(GiB\)\. This can be a number from 1\-1,024 for `standard`, 4\-16,384 for `io1`, 1\-16,384 for `gp2`, and 500\-16,384 for `st1` and `sc1`\.   
If you create a volume from a snapshot and you don't specify a volume size, the default is the snapshot size\.   
You must specify either a `VolumeSize` or a `SnapshotId`\. If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Required*: Conditional  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `16384`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-as-launchconfig-blockdev-template-volumetype"></a>
The volume type, which can be `standard` for Magnetic, `io1` for Provisioned IOPS SSD, `gp2` for General Purpose SSD, `st1` for Throughput Optimized HDD, or `sc1` for Cold HDD\. For more information, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
Valid values: `standard` \| `io1` \| `gp2` \| `st1` \| `sc1`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-as-launchconfig-blockdev-template--seealso"></a>
+ [Required CMK key policy for use with encrypted volumes](https://docs.aws.amazon.com/autoscaling/ec2/userguide/key-policy-requirements-EBS-encryption.html) in the *Amazon EC2 Auto Scaling User Guide*
+ [Using encryption with EBS\-backed AMIs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIEncryption.html) in the *Amazon EC2 User Guide for Linux Instances*

