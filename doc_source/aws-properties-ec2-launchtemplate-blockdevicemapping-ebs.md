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
The number of I/O operations per second \(IOPS\)\. For `gp3`, `io1`, and `io2` volumes, this represents the number of IOPS that are provisioned for the volume\. For `gp2` volumes, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\.  
The following are the supported values for each volume type:  
+  `gp3`: 3,000\-16,000 IOPS
+  `io1`: 100\-64,000 IOPS
+  `io2`: 100\-64,000 IOPS
For `io1` and `io2` volumes, we guarantee 64,000 IOPS only for [Instances built on the Nitro System](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\.  
This parameter is required for `io1` and `io2` volumes\. The default for `gp3` volumes is 3,000 IOPS\. This parameter is not supported for `gp2`, `st1`, `sc1`, or `standard` volumes\.  
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
The size of the volume, in GiBs\. You must specify either a snapshot ID or a volume size\. If you specify a snapshot, the default is the snapshot size\. You can specify a volume size that is equal to or larger than the snapshot size\.  
The following are the supported volumes sizes for each volume type:  
+  `gp2` and `gp3`: 1\-16,384
+  `io1` and `io2`: 4\-16,384
+  `st1` and `sc1`: 125\-16,384
+  `standard`: 1\-1,024
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs-volumetype"></a>
The volume type\. The default is `gp2`\. For more information, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `gp2 | gp3 | io1 | io2 | sc1 | st1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-ebs--seealso"></a>
+  [ LaunchTemplateEbsBlockDeviceRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateEbsBlockDeviceRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 

