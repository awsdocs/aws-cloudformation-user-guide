# Amazon EMR EbsConfiguration EbsBlockDeviceConfig VolumeSpecification<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification"></a>

`VolumeSpecification` is a property of the [Amazon EMR EbsConfiguration](aws-properties-emr-ebsconfiguration.md) property that configures the Amazon Elastic Block Store \(Amazon EBS\) volumes that Amazon EMR \(Amazon EMR\) associates with your instances\.

## Syntax<a name="w3ab2c21c14e1153b5"></a>

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

## Properties<a name="w3ab2c21c14e1153b7"></a>

`Iops`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. For more information, see [Iops](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: Integer

`SizeInGB`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-sizeingb"></a>
The volume size, in Gibibytes \(GiB\)\. For more information about specifying the volume size, see [VolumeSize](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required*: Yes  
*Type*: Integer

`VolumeType`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-volumetype"></a>
The volume type, such as `standard` or `io1`\. For more information about specifying the volume type, see [VolumeType](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required*: Yes  
*Type*: String