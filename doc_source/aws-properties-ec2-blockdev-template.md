# AWS::EC2::Instance Ebs<a name="aws-properties-ec2-blockdev-template"></a>

Specifies a block device for an EBS volume\.

 `Ebs` is a property of the [ Amazon EC2 BlockDeviceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-blockdev-mapping.html) property\.

## Syntax<a name="aws-properties-ec2-blockdev-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-blockdev-template-syntax.json"></a>

```
{
  "[DeleteOnTermination](#cfn-ec2-blockdev-template-deleteontermination)" : Boolean,
  "[Encrypted](#cfn-ec2-blockdev-template-encrypted)" : Boolean,
  "[Iops](#cfn-ec2-blockdev-template-iops)" : Integer,
  "[SnapshotId](#cfn-ec2-blockdev-template-snapshotid)" : String,
  "[VolumeSize](#cfn-ec2-blockdev-template-volumesize)" : Integer,
  "[VolumeType](#cfn-ec2-blockdev-template-volumetype)" : String
}
```

### YAML<a name="aws-properties-ec2-blockdev-template-syntax.yaml"></a>

```
  [DeleteOnTermination](#cfn-ec2-blockdev-template-deleteontermination): Boolean
  [Encrypted](#cfn-ec2-blockdev-template-encrypted): Boolean
  [Iops](#cfn-ec2-blockdev-template-iops): Integer
  [SnapshotId](#cfn-ec2-blockdev-template-snapshotid): String
  [VolumeSize](#cfn-ec2-blockdev-template-volumesize): Integer
  [VolumeType](#cfn-ec2-blockdev-template-volumetype): String
```

## Properties<a name="aws-properties-ec2-blockdev-template-properties"></a>

`DeleteOnTermination`  <a name="cfn-ec2-blockdev-template-deleteontermination"></a>
Indicates whether the EBS volume is deleted on instance termination\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-ec2-blockdev-template-encrypted"></a>
Indicates whether the volume is encrypted\. Encrypted Amazon EBS volumes can only be attached to instance types that support Amazon EBS encryption\. Volumes that are created from encrypted snapshots are automatically encrypted\. You cannot create an encrypted volume from an unencrypted snapshot or vice versa\. If your AMI uses encrypted volumes, you can only launch the AMI on supported instance types\. For more information, see [ Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-ec2-blockdev-template-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. For `io1` volumes, this represents the number of IOPS that are provisioned for the volume\. For `gp2` volumes, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\. For more information, see [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Constraints: Range is 100\-16,000 IOPS for `gp2` volumes and 100 to 64,000IOPS for `io1` volumes in most Regions\. Maximum `io1` IOPS of 64,000 is guaranteed only on [Nitro\-based instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\. For more information, see [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Condition: This parameter is required for requests to create `io1` volumes; it is not used in requests to create `gp2`, `st1`, `sc1`, or `standard` volumes\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-ec2-blockdev-template-snapshotid"></a>
The ID of the snapshot\.  
If you specify both `SnapshotId` and `VolumeSize`,`VolumeSize` must be equal or greater than the size of the snapshot\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-ec2-blockdev-template-volumesize"></a>
The size of the volume, in GiB\.  
Default: If you're creating the volume from a snapshot and don't specify a volume size, the default is the snapshot size\.  
Constraints: 1\-16384 for General Purpose SSD \(`gp2`\), 4\-16384 for Provisioned IOPS SSD \(`io1`\), 500\-16384 for Throughput Optimized HDD \(`st1`\), 500\-16384 for Cold HDD \(`sc1`\), and 1\-1024 for Magnetic \(`standard`\) volumes\. If you specify a snapshot, the volume size must be equal to or larger than the snapshot size\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-blockdev-template-volumetype"></a>
The volume type\. If you set the type to `io1`, you must also set the **Iops** property\.  
Default: `standard`   
*Required*: No  
*Type*: String  
*Allowed Values*: `gp2 | io1 | sc1 | st1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-ec2-blockdev-template--examples"></a>

### Creating an EBS volume from a snapshot<a name="aws-properties-ec2-blockdev-template--examples--Creating_an_EBS_volume_from_a_snapshot"></a>

This example creates a 50GB io1 EBS volume from a snapshot, and configures it to support 1000 IOPS and to persist after terminating the instance to which it is attached\.

#### JSON<a name="aws-properties-ec2-blockdev-template--examples--Creating_an_EBS_volume_from_a_snapshot--json"></a>

```
{
    "DeviceName": "/dev/sdc",
    "Ebs": {
        "SnapshotId": "snap-xxxxxx",
        "VolumeSize": "50",
        "VolumeType": "io1",
        "Iops": "1000",
        "DeleteOnTermination": "false"
    }
}
```

## See Also<a name="aws-properties-ec2-blockdev-template--seealso"></a>
+  [ CreateVolume](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVolume.html) in the *Amazon Elastic Compute Cloud API Reference*