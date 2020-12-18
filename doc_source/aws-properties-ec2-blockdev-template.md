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
  "[KmsKeyId](#cfn-ec2-instance-ebs-kmskeyid)" : String,
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
  [KmsKeyId](#cfn-ec2-instance-ebs-kmskeyid): String
  [SnapshotId](#cfn-ec2-blockdev-template-snapshotid): String
  [VolumeSize](#cfn-ec2-blockdev-template-volumesize): Integer
  [VolumeType](#cfn-ec2-blockdev-template-volumetype): String
```

## Properties<a name="aws-properties-ec2-blockdev-template-properties"></a>

`DeleteOnTermination`  <a name="cfn-ec2-blockdev-template-deleteontermination"></a>
Indicates whether the EBS volume is deleted on instance termination\. For more information, see [Preserving Amazon EBS volumes on instance termination](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/terminating-instances.html#preserving-volumes-on-termination) in the *Amazon EC2 User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-ec2-blockdev-template-encrypted"></a>
Indicates whether the volume should be encrypted\. The effect of setting the encryption state to `true` depends on the volume origin \(new or from a snapshot\), starting encryption state, ownership, and whether encryption by default is enabled\. For more information, see [Encryption by default](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#encryption-by-default) in the *Amazon Elastic Compute Cloud User Guide*\.  
Encrypted Amazon EBS volumes must be attached to instances that support Amazon EBS encryption\. For more information, see [Supported instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#EBSEncryption_supported_instances)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-ec2-blockdev-template-iops"></a>
The number of I/O operations per second \(IOPS\)\. For `gp3`, `io1`, and `io2` volumes, this represents the number of IOPS that are provisioned for the volume\. For `gp2` volumes, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\.  
The following are the supported values for each volume type:  
+  `gp3`: 3,000\-16,000 IOPS
+  `io1`: 100\-64,000 IOPS
+  `io2`: 100\-64,000 IOPS
For `io1` and `io2` volumes, we guarantee 64,000 IOPS only for [Instances built on the Nitro System](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\.  
This parameter is required for `io1` and `io2` volumes\. The default for `gp3` volumes is 3,000 IOPS\. This parameter is not supported for `gp2`, `st1`, `sc1`, or `standard` volumes\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-ec2-instance-ebs-kmskeyid"></a>
The identifier of the AWS Key Management Service \(AWS KMS\) customer managed CMK to use for Amazon EBS encryption\. If `KmsKeyId` is specified, the encrypted state must be `true`\. If the encrypted state is `true` but you do not specify `KmsKeyId`, your AWS managed CMK for EBS is used\.  
You can specify the CMK using any of the following:  
+ Key ID\. For example, 1234abcd\-12ab\-34cd\-56ef\-1234567890ab\.
+ Key alias\. For example, alias/ExampleAlias\.
+ Key ARN\. For example, arn:aws:kms:us\-east\-1:012345678910:1234abcd\-12ab\-34cd\-56ef\-1234567890ab\.
+ Alias ARN\. For example, arn:aws:kms:us\-east\-1:012345678910:alias/ExampleAlias\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotId`  <a name="cfn-ec2-blockdev-template-snapshotid"></a>
The ID of the snapshot\.  
If you specify both `SnapshotId` and `VolumeSize`,`VolumeSize` must be equal or greater than the size of the snapshot\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-ec2-blockdev-template-volumesize"></a>
The size of the volume, in GiBs\. You must specify either a snapshot ID or a volume size\. If you specify a snapshot, the default is the snapshot size\. You can specify a volume size that is equal to or larger than the snapshot size\.  
The following are the supported volumes sizes for each volume type:  
+  `gp2` and `gp3`:1\-16,384
+  `io1` and `io2`: 4\-16,384
+  `st1` and `sc1`: 125\-16,384
+  `standard`: 1\-1,024
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-blockdev-template-volumetype"></a>
The volume type\. For more information, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon EC2 User Guide*\. If the volume type is `io1` or `io2`, you must specify the IOPS that the volume supports\.  
*Required*: No  
*Type*: String  
*Allowed values*: `gp2 | gp3 | io1 | io2 | sc1 | st1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-ec2-blockdev-template--examples"></a>

### Creating an EBS volume from a snapshot<a name="aws-properties-ec2-blockdev-template--examples--Creating_an_EBS_volume_from_a_snapshot"></a>

This example creates a 50GB io1 EBS volume from a snapshot, and configures it to support 1000 IOPS and to persist after terminating the instance to which it is attached\.

#### JSON<a name="aws-properties-ec2-blockdev-template--examples--Creating_an_EBS_volume_from_a_snapshot--json"></a>

```
{
    "DeviceName": "/dev/sdc",
    "Ebs": {
        "SnapshotId": "snap-xxxxxxxx",
        "VolumeSize": "50",
        "VolumeType": "io1",
        "Iops": "1000",
        "DeleteOnTermination": "false"
    }
}
```

#### YAML<a name="aws-properties-ec2-blockdev-template--examples--Creating_an_EBS_volume_from_a_snapshot--yaml"></a>

```
BlockDeviceMappings:
  - DeviceName: /dev/sdc
    Ebs:
      SnapshotId: snap-xxxxxxxx
      VolumeSize: 50
      VolumeType: io1
      Iops: 1000
      DeleteOnTermination: false
```

## See also<a name="aws-properties-ec2-blockdev-template--seealso"></a>
+  [ CreateVolume](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVolume.html) in the *Amazon Elastic Compute Cloud API Reference*