# Amazon Elastic Compute Cloud SpotFleet Ebs<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs"></a>

`Ebs` is a property of the [Amazon Elastic Compute Cloud SpotFleet BlockDeviceMappings](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings.md) property that defines a block device for an Amazon Elastic Block Store \(Amazon EBS\) volume\.

## Syntax<a name="w3ab2c21c14d782b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-syntax.json"></a>

```
{
  "[DeleteOnTermination](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-deleteontermination)" : Boolean,
  "[Encrypted](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-encrypted)" : Boolean,
  "[Iops](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-iops)" : Integer,
  "[SnapshotId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-snapshotid)" : String,
  "[VolumeSize](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-volumesize)" : Integer,
  "[VolumeType](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-volumetype)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-syntax.yaml"></a>

```
[DeleteOnTermination](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-deleteontermination): Boolean
[Encrypted](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-encrypted): Boolean
[Iops](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-iops): Integer
[SnapshotId](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-snapshotid): String
[VolumeSize](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-volumesize): Integer
[VolumeType](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-volumetype): String
```

## Properties<a name="w3ab2c21c14d782b7"></a>

`DeleteOnTermination`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-deleteontermination"></a>
Indicates whether to delete the volume when the instance is terminated\.  
*Required*: No  
*Type*: Boolean

`Encrypted`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-encrypted"></a>
Indicates whether the EBS volume is encrypted\. Encrypted Amazon EBS volumes can be attached only to instances that support Amazon EBS encryption\.  
*Required*: No  
*Type*: Boolean

`Iops`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. For more information, see [Iops](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: Integer

`SnapshotId`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-snapshotid"></a>
The snapshot ID of the volume that you want to use\. If you specify both the `SnapshotId` and `VolumeSize` properties, `VolumeSize` must be equal to or greater than the size of the snapshot\.  
*Required*: No  
*Type*: String

`VolumeSize`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-volumesize"></a>
The volume size, in Gibibytes \(GiB\)\. If you specify both the `SnapshotId` and `VolumeSize` properties, `VolumeSize` must be equal to or greater than the size of the snapshot\. For more information about specifying the volume size, see [VolumeSize](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: Integer

`VolumeType`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs-volumetype"></a>
The volume type\. For more information about specifying the volume type, see [VolumeType](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: String