# AWS::EMR::InstanceGroupConfig VolumeSpecification<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification"></a>

`VolumeSpecification` is a subproperty of the `EbsBlockDeviceConfig` property type\. `VolumeSecification` determines the volume type, IOPS, and size \(GiB\) for EBS volumes attached to EC2 instances\.

## Syntax<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-syntax.json"></a>

```
{
  "[Iops](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-iops)" : Integer,
  "[SizeInGB](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-sizeingb)" : Integer,
  "[VolumeType](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-volumetype)" : String
}
```

### YAML<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-syntax.yaml"></a>

```
  [Iops](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-iops): Integer
  [SizeInGB](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-sizeingb): Integer
  [VolumeType](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-volumetype): String
```

## Properties<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-properties"></a>

`Iops`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeInGB`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-sizeingb"></a>
The volume size, in gibibytes \(GiB\)\. This can be a number from 1 \- 1024\. If the volume type is EBS\-optimized, the minimum value is 10\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-volumetype"></a>
The volume type\. Volume types supported are gp2, io1, standard\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)