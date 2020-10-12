# AWS::EC2::LaunchTemplate Ebs<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-ebs"></a>

Parameters for a block device for an EBS volume in an Amazon EC2 launch template\.

 `Ebs` is a property of [ AWS::EC2::LaunchTemplate BlockDeviceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-blockdevicemapping.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-ebs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-ebs-syntax.json"></a>

```
{
  "[DeleteOnTermination](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-deleteontermination)" : Boolean,
  "[Encrypted](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-encrypted)" : Boolean,
  "[Iops](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-iops)" : Integer,
  "[KmsKeyId](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-kmskeyid)" : String,
  "[SnapshotId](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-snapshotid)" : String,
  "[VolumeSize](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-volumesize)" : Integer,
  "[VolumeType](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-volumetype)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-ebs-syntax.yaml"></a>

```
  [DeleteOnTermination](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-deleteontermination): Boolean
  [Encrypted](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-encrypted): Boolean
  [Iops](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-iops): Integer
  [KmsKeyId](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-kmskeyid): String
  [SnapshotId](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-snapshotid): String
  [VolumeSize](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-volumesize): Integer
  [VolumeType](#cfn-ec2-launchtemplate-blockdevicemapping-ebs-volumetype): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-ebs-properties"></a>

`DeleteOnTermination`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs-deleteontermination"></a>
Indicates whether the EBS volume is deleted on instance termination\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs-encrypted"></a>
Indicates whether the EBS volume is encrypted\. Encrypted volumes can only be attached to instances that support Amazon EBS encryption\. If you are creating a volume from a snapshot, you can't specify an encryption value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs-iops"></a>
The number of I/O operations per second \(IOPS\) to provision for an `io1` or `io2` volume, with a maximum ratio of 50 IOPS/GiB for `io1`, and 500 IOPS/GiB for `io2`\. Range is 100 to 64,000 IOPS for volumes in most Regions\. Maximum IOPS of 64,000 is guaranteed only on [Nitro\-based instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\. For more information, see [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
This parameter is valid only for Provisioned IOPS SSD \(`io1` and `io2`\) volumes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs-kmskeyid"></a>
The ARN of the symmetric AWS Key Management Service \(AWS KMS\) CMK used for encryption\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs-snapshotid"></a>
The ID of the snapshot\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs-volumesize"></a>
The size of the volume, in GiB\.  
Default: If you're creating the volume from a snapshot and don't specify a volume size, the default is the snapshot size\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs-volumetype"></a>
The volume type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `gp2 | io1 | io2 | sc1 | st1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-ebs--seealso"></a>
+  [ LaunchTemplateEbsBlockDeviceRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateEbsBlockDeviceRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 