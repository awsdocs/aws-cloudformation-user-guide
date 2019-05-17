# AWS::EC2::SpotFleet EbsBlockDevice<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs"></a>

Describes a block device for an EBS volume\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-syntax.json"></a>

```
{
  "[DeleteOnTermination](#cfn-ec2-spotfleet-ebsblockdevice-deleteontermination)" : Boolean,
  "[Encrypted](#cfn-ec2-spotfleet-ebsblockdevice-encrypted)" : Boolean,
  "[Iops](#cfn-ec2-spotfleet-ebsblockdevice-iops)" : Integer,
  "[SnapshotId](#cfn-ec2-spotfleet-ebsblockdevice-snapshotid)" : String,
  "[VolumeSize](#cfn-ec2-spotfleet-ebsblockdevice-volumesize)" : Integer,
  "[VolumeType](#cfn-ec2-spotfleet-ebsblockdevice-volumetype)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-syntax.yaml"></a>

```
  [DeleteOnTermination](#cfn-ec2-spotfleet-ebsblockdevice-deleteontermination): Boolean
  [Encrypted](#cfn-ec2-spotfleet-ebsblockdevice-encrypted): Boolean
  [Iops](#cfn-ec2-spotfleet-ebsblockdevice-iops): Integer
  [SnapshotId](#cfn-ec2-spotfleet-ebsblockdevice-snapshotid): String
  [VolumeSize](#cfn-ec2-spotfleet-ebsblockdevice-volumesize): Integer
  [VolumeType](#cfn-ec2-spotfleet-ebsblockdevice-volumetype): String
```

## Properties<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-properties"></a>

`DeleteOnTermination`  <a name="cfn-ec2-spotfleet-ebsblockdevice-deleteontermination"></a>
Indicates whether the EBS volume is deleted on instance termination\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-ec2-spotfleet-ebsblockdevice-encrypted"></a>
Indicates whether the encryption state of an EBS volume is to be changed while being restored from a backing snapshot\. The default effect of setting this parameter to `true` or leaving it unset depends on the origin, starting encryption state, and ownership of the volume\. Each default case can be overridden by specifying a customer master key \(CMK\) as argument to the `KmsKeyId` parameter in addition to setting `Encrypted` = `true`\. For a complete list of possible encryption cases, see [Amazon EBS Encryption](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html)\.   
In no case can you remove encryption from an encrypted volume\.  
Encrypted volumes can only be attached to instances that support Amazon EBS encryption\. For more information, see [Supported Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#EBSEncryption_supported_instances)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-ec2-spotfleet-ebsblockdevice-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. For `io1` volumes, this represents the number of IOPS that are provisioned for the volume\. For `gp2` volumes, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\. For more information, see [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Constraints: Range is 100\-16,000 IOPS for `gp2` volumes and 100 to 64,000IOPS for `io1` volumes in most Regions\. Maximum `io1`IOPS of 64,000 is guaranteed only on [Nitro\-based instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\. For more information, see [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Condition: This parameter is required for requests to create `io1` volumes; it is not used in requests to create `gp2`, `st1`, `sc1`, or `standard` volumes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-ec2-spotfleet-ebsblockdevice-snapshotid"></a>
The ID of the snapshot\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-ec2-spotfleet-ebsblockdevice-volumesize"></a>
The size of the volume, in GiB\.  
Default: If you're creating the volume from a snapshot and don't specify a volume size, the default is the snapshot size\.  
Constraints: 1\-16384 for General Purpose SSD \(`gp2`\), 4\-16384 for Provisioned IOPS SSD \(`io1`\), 500\-16384 for Throughput Optimized HDD \(`st1`\), 500\-16384 for Cold HDD \(`sc1`\), and 1\-1024 for Magnetic \(`standard`\) volumes\. If you specify a snapshot, the volume size must be equal to or larger than the snapshot size\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-spotfleet-ebsblockdevice-volumetype"></a>
The volume type\. If you set the type to `io1`, you must also set the **Iops** property\.  
Default: `standard`   
*Required*: No  
*Type*: String  
*Allowed Values*: `gp2 | io1 | sc1 | st1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)