# AWS::EMR::InstanceFleetConfig VolumeSpecification<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification"></a>

`VolumeSpecification` is a subproperty of the `EbsBlockDeviceConfig` property type\. `VolumeSecification` determines the volume type, IOPS, and size \(GiB\) for EBS volumes attached to EC2 instances\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification-syntax.json"></a>

```
{
  "[Iops](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-iops)" : Integer,
  "[SizeInGB](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-sizeingb)" : Integer,
  "[VolumeType](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-volumetype)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification-syntax.yaml"></a>

```
  [Iops](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-iops): Integer
  [SizeInGB](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-sizeingb): Integer
  [VolumeType](#cfn-elasticmapreduce-instancefleetconfig-volumespecification-volumetype): String
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-volumespecification-properties"></a>

`Iops`  <a name="cfn-elasticmapreduce-instancefleetconfig-volumespecification-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SizeInGB`  <a name="cfn-elasticmapreduce-instancefleetconfig-volumespecification-sizeingb"></a>
The volume size, in gibibytes \(GiB\)\. This can be a number from 1 \- 1024\. If the volume type is EBS\-optimized, the minimum value is 10\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeType`  <a name="cfn-elasticmapreduce-instancefleetconfig-volumespecification-volumetype"></a>
The volume type\. Volume types supported are gp2, io1, standard\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)