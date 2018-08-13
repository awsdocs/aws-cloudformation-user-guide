# Amazon EC2 LaunchTemplate Ebs<a name="aws-properties-ec2-launchtemplate-ebs"></a>

<a name="aws-properties-ec2-launchtemplate-ebs-description"></a>The `Ebs` property type specifies parameters for a block device for an EBS volume in a Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-ebs-inheritance"></a> `Ebs` is a property of the [Amazon EC2 LaunchTemplate BlockDeviceMapping](aws-properties-ec2-launchtemplate-blockdevicemapping.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-ebs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-ebs-syntax.json"></a>

```
{
  "[SnapshotId](#cfn-ec2-launchtemplate-ebs-snapshotid)" : String,
  "[VolumeType](#cfn-ec2-launchtemplate-ebs-volumetype)" : String,
  "[KmsKeyId](#cfn-ec2-launchtemplate-ebs-kmskeyid)" : String,
  "[Encrypted](#cfn-ec2-launchtemplate-ebs-encrypted)" : Boolean,
  "[Iops](#cfn-ec2-launchtemplate-ebs-iops)" : Integer,
  "[VolumeSize](#cfn-ec2-launchtemplate-ebs-volumesize)" : Integer,
  "[DeleteOnTermination](#cfn-ec2-launchtemplate-ebs-deleteontermination)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-ebs-syntax.yaml"></a>

```
[SnapshotId](#cfn-ec2-launchtemplate-ebs-snapshotid): String
[VolumeType](#cfn-ec2-launchtemplate-ebs-volumetype): String
[KmsKeyId](#cfn-ec2-launchtemplate-ebs-kmskeyid): String
[Encrypted](#cfn-ec2-launchtemplate-ebs-encrypted): Boolean
[Iops](#cfn-ec2-launchtemplate-ebs-iops): Integer
[VolumeSize](#cfn-ec2-launchtemplate-ebs-volumesize): Integer
[DeleteOnTermination](#cfn-ec2-launchtemplate-ebs-deleteontermination): Boolean
```

## Properties<a name="aws-properties-ec2-launchtemplate-ebs-properties"></a>

`DeleteOnTermination`  <a name="cfn-ec2-launchtemplate-ebs-deleteontermination"></a>
Indicates whether the EBS volume is deleted on instance termination\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Encrypted`  <a name="cfn-ec2-launchtemplate-ebs-encrypted"></a>
Indicates whether the EBS volume is encrypted\. Encrypted volumes can only be attached to instances that support Amazon EBS encryption\. If you are creating a volume from a snapshot, you can't specify an encryption value\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Iops`  <a name="cfn-ec2-launchtemplate-ebs-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. For io1, this represents the number of IOPS that are provisioned for the volume\. For gp2, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\. For more information about General Purpose SSD baseline performance, I/O credits, and bursting, see [Amazon EBS Volume Types](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
Condition: This parameter is required for requests to create io1 volumes; it is not used in requests to create gp2, st1, sc1, or standard volumes\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KmsKeyId`  <a name="cfn-ec2-launchtemplate-ebs-kmskeyid"></a>
The ARN of the AWS Key Management Service \(AWS KMS\) CMK used for encryption\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SnapshotId`  <a name="cfn-ec2-launchtemplate-ebs-snapshotid"></a>
The ID of the snapshot\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VolumeSize`  <a name="cfn-ec2-launchtemplate-ebs-volumesize"></a>
The size of the volume, in GiB\.  
Default: If you're creating the volume from a snapshot and don't specify a volume size, the default is the snapshot size\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VolumeType`  <a name="cfn-ec2-launchtemplate-ebs-volumetype"></a>
The volume type\.  
Valid values include: `standard`, `io1`, `gp2`, `sc1`, and `st1`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-ebs-seealso"></a>
+ [LaunchTemplateEbsBlockDeviceRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateEbsBlockDeviceRequest.html) in the *Amazon EC2 API Reference*