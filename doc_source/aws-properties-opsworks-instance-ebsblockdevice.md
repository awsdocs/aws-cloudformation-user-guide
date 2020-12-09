# AWS::OpsWorks::Instance EbsBlockDevice<a name="aws-properties-opsworks-instance-ebsblockdevice"></a>

Describes an Amazon EBS volume\. This data type maps directly to the Amazon EC2 [EbsBlockDevice](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) data type\.

## Syntax<a name="aws-properties-opsworks-instance-ebsblockdevice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-instance-ebsblockdevice-syntax.json"></a>

```
{
  "[DeleteOnTermination](#cfn-opsworks-instance-ebsblockdevice-deleteontermination)" : Boolean,
  "[Iops](#cfn-opsworks-instance-ebsblockdevice-iops)" : Integer,
  "[SnapshotId](#cfn-opsworks-instance-ebsblockdevice-snapshotid)" : String,
  "[VolumeSize](#cfn-opsworks-instance-ebsblockdevice-volumesize)" : Integer,
  "[VolumeType](#cfn-opsworks-instance-ebsblockdevice-volumetype)" : String
}
```

### YAML<a name="aws-properties-opsworks-instance-ebsblockdevice-syntax.yaml"></a>

```
  [DeleteOnTermination](#cfn-opsworks-instance-ebsblockdevice-deleteontermination): Boolean
  [Iops](#cfn-opsworks-instance-ebsblockdevice-iops): Integer
  [SnapshotId](#cfn-opsworks-instance-ebsblockdevice-snapshotid): String
  [VolumeSize](#cfn-opsworks-instance-ebsblockdevice-volumesize): Integer
  [VolumeType](#cfn-opsworks-instance-ebsblockdevice-volumetype): String
```

## Properties<a name="aws-properties-opsworks-instance-ebsblockdevice-properties"></a>

`DeleteOnTermination`  <a name="cfn-opsworks-instance-ebsblockdevice-deleteontermination"></a>
Whether the volume is deleted on instance termination\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-opsworks-instance-ebsblockdevice-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. For more information, see [EbsBlockDevice](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-opsworks-instance-ebsblockdevice-snapshotid"></a>
The snapshot ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeSize`  <a name="cfn-opsworks-instance-ebsblockdevice-volumesize"></a>
The volume size, in GiB\. For more information, see [EbsBlockDevice](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-opsworks-instance-ebsblockdevice-volumetype"></a>
The volume type\. `gp2` for General Purpose \(SSD\) volumes, `io1` for Provisioned IOPS \(SSD\) volumes, `st1` for Throughput Optimized hard disk drives \(HDD\), `sc1` for Cold HDD,and `standard` for Magnetic volumes\.  
If you specify the `io1` volume type, you must also specify a value for the `Iops` attribute\. The maximum ratio of provisioned IOPS to requested volume size \(in GiB\) is 50:1\. AWS uses the default volume size \(in GiB\) specified in the AMI attributes to set IOPS to 50 x \(volume size\)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `gp2 | io1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)