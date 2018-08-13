# Amazon EC2 Auto Scaling EBS Block Device Property Type<a name="aws-properties-as-launchconfig-blockdev-template"></a>

The AutoScaling EBS Block Device type is an embedded property of the [Amazon EC2 Auto Scaling Block Device Mapping](aws-properties-as-launchconfig-blockdev-mapping.md) type\.

## Syntax<a name="w3ab2c21c14c98b5"></a>

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

## Properties<a name="w3ab2c21c14c98b7"></a>

`DeleteOnTermination`  <a name="cfn-as-launchconfig-blockdev-template-deleteonterm"></a>
Indicates whether to delete the volume when the instance is terminated\. By default, Auto Scaling uses `true`\.  
*Required*: No  
*Type*: Boolean

`Encrypted`  <a name="cfn-as-launchconfig-blockdev-template-encrypted"></a>
Indicates whether the volume is encrypted\. Encrypted EBS volumes must be attached to instances that support Amazon EBS encryption\. Volumes that you create from encrypted snapshots are automatically encrypted\. You cannot create an encrypted volume from an unencrypted snapshot or an unencrypted volume from an encrypted snapshot\.  
*Required*: No  
*Type*: Boolean

`Iops`  <a name="cfn-as-launchconfig-blockdev-template-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. The maximum ratio of IOPS to volume size is 30\.  
*Required*: No  
*Type*: Integer\.

`SnapshotId`  <a name="cfn-as-launchconfig-blockdev-template-snapshotid"></a>
The snapshot ID of the volume to use\.  
*Required*: Conditional If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Type*: String

`VolumeSize`  <a name="cfn-as-launchconfig-blockdev-template-volumesize"></a>
The volume size, in Gibibytes \(GiB\)\. This can be a number from 1 – 1024\. If the volume type is EBS optimized, the minimum value is 10\. For more information about specifying the volume type, see EbsOptimized in [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md)\.  
*Required*: Conditional If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Type*: Integer\.  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`VolumeType`  <a name="cfn-as-launchconfig-blockdev-template-volumetype"></a>
The volume type\. By default, Auto Scaling uses the `standard` volume type\. For more information, see [Ebs](http://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_Ebs.html) in the *Amazon EC2 Auto Scaling API Reference*\.  
*Required*: No  
*Type*: String

## Examples<a name="w3ab2c21c14c98b9"></a>

For AutoScaling EBS Block Device snippets, see [Auto Scaling Launch Configuration Resource](quickref-autoscaling.md#scenario-as-launch-config)\.