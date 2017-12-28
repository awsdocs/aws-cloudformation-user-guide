# AWS CloudFormation AutoScaling EBS Block Device Property Type<a name="aws-properties-as-launchconfig-blockdev-template"></a>

The AutoScaling EBS Block Device type is an embedded property of the  type\.

## Syntax<a name="w3ab2c21c14c74b5"></a>

### JSON<a name="aws-properties-as-launchconfig-blockdev-template-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-launchconfig-blockdev-template-deleteonterm)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-launchconfig-blockdev-template-encrypted)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-launchconfig-blockdev-template-iops)" : Integer,
  "SnapshotId" : String,
  "VolumeSize" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-launchconfig-blockdev-template-volumetype)" : String
}
```

### YAML<a name="aws-properties-as-launchconfig-blockdev-template-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-launchconfig-blockdev-template-deleteonterm): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-launchconfig-blockdev-template-encrypted): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-launchconfig-blockdev-template-iops): Integer
SnapshotId: String
VolumeSize: Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-as-launchconfig-blockdev-template-volumetype): String
```

## Properties<a name="w3ab2c21c14c74b7"></a>

`DeleteOnTermination`  
Indicates whether to delete the volume when the instance is terminated\. By default, Auto Scaling uses `true`\.  
*Required: *No  
*Type*: Boolean

`Encrypted`  
Indicates whether the volume is encrypted\. Encrypted EBS volumes must be attached to instances that support Amazon EBS encryption\. Volumes that you create from encrypted snapshots are automatically encrypted\. You cannot create an encrypted volume from an unencrypted snapshot or an unencrypted volume from an encrypted snapshot\.  
*Required: *No  
*Type*: Boolean

`Iops`  
The number of I/O operations per second \(IOPS\) that the volume supports\. The maximum ratio of IOPS to volume size is 30\.  
*Required: *No  
*Type*: Integer\.

`SnapshotId`  
The snapshot ID of the volume to use\.  
*Required: *Conditional If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Type*: String

`VolumeSize`  
The volume size, in Gibibytes \(GiB\)\. This can be a number from 1 – 1024\. If the volume type is EBS optimized, the minimum value is 10\. For more information about specifying the volume type, see EbsOptimized in [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md)\.  
*Required: *Conditional If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Type*: Integer\.  
*Update requires*: Some interruptions

`VolumeType`  
The volume type\. By default, Auto Scaling uses the `standard` volume type\. For more information, see [Ebs](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_Ebs.html) in the *Auto Scaling API Reference*\.  
*Required: *No  
*Type*: String

## Examples<a name="w3ab2c21c14c74b9"></a>

For AutoScaling EBS Block Device snippets, see \.