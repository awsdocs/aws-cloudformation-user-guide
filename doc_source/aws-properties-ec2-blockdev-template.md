# Amazon Elastic Block Store Block Device Property<a name="aws-properties-ec2-blockdev-template"></a>

The Amazon Elastic Block Store block device type is an embedded property of the  property\.

## Syntax<a name="w3ab2c21c14d559b5"></a>

### JSON<a name="aws-properties-ec2-blockdev-template-syntax.json"></a>

```
{
   "DeleteOnTermination" : Boolean,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-blockdev-template-encrypted)" : Boolean,
   "Iops" : Number,
   "SnapshotId" : String,
   "VolumeSize" : String,
   "VolumeType" : String
}
```

### YAML<a name="aws-properties-ec2-blockdev-template-syntax.yaml"></a>

```
DeleteOnTermination: Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-blockdev-template-encrypted): Boolean
Iops: Number
SnapshotId: String
VolumeSize: String
VolumeType: String
```

## Properties<a name="w3ab2c21c14d559b7"></a>

`DeleteOnTermination`  
Determines whether to delete the volume on instance termination\. The default value is `true`\.  
*Required: *No  
*Type*: Boolean

`Encrypted`  
Indicates whether the volume is encrypted\. Encrypted Amazon EBS volumes can only be attached to instance types that support Amazon EBS encryption\. Volumes that are created from encrypted snapshots are automatically encrypted\. You cannot create an encrypted volume from an unencrypted snapshot or vice versa\. If your AMI uses encrypted volumes, you can only launch the AMI on supported instance types\. For more information, see [Amazon EBS encryption](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required: *No  
*Type*: Boolean

`Iops`  
The number of I/O operations per second \(IOPS\) that the volume supports\. This can be an integer from 100 – 20000\.  
*Required: *Conditional Required when the volume type is `io1`; not used with other volume types\.  
*Type*: Number

`SnapshotId`  
The snapshot ID of the volume to use to create a block device\.  
*Required: *Conditional If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Type*: String

`VolumeSize`  
The volume size, in gibibytes \(GiB\)\. For valid values, see the `Size` parameter for the [CreateVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) action in the *Amazon EC2 API Reference*\.  
*Required: *Conditional If you specify both `SnapshotId` and `VolumeSize`, `VolumeSize` must be equal or greater than the size of the snapshot\.  
*Type*: String  
*Update requires*: Some interruptions

`VolumeType`  
The volume type\. If you set the type to `io1`, you must also set the `Iops` property\. For valid values, see the `VolumeType` parameter for the [CreateVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) action in the *Amazon EC2 API Reference*\.  
*Required: *No  
*Type*: String

## Example<a name="w3ab2c21c14d559b9"></a>

```
{
   "DeviceName":"/dev/sdc",
   "Ebs":{
      "SnapshotId":"snap-xxxxxx",
      "VolumeSize":"50",
      "VolumeType":"io1",
      "Iops":"1000",
      "DeleteOnTermination":"false"
   }
}
```

## See Also<a name="w3ab2c21c14d559c11"></a>

+ [CreateVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) in the *Amazon Elastic Compute Cloud API Reference*