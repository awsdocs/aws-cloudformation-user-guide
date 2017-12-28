# Amazon EMR EbsConfiguration EbsBlockDeviceConfig VolumeSpecification<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification"></a>

`VolumeSpecification` is a property of the [Amazon EMR EbsConfiguration](aws-properties-emr-ebsconfiguration.md) property that configures the Amazon Elastic Block Store \(Amazon EBS\) volumes that Amazon EMR \(Amazon EMR\) associates with your instances\.

## Syntax<a name="w3ab2c21c14d962b5"></a>

### JSON<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-iops)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-sizeingb)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-volumetype)" : String
}
```

### YAML<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-iops): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-sizeingb): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification-volumetype): String
```

## Properties<a name="w3ab2c21c14d962b7"></a>

`Iops`  
The number of I/O operations per second \(IOPS\) that the volume supports\. For more information, see [Iops](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required: *No  
*Type*: Integer

`SizeInGB`  
The volume size, in Gibibytes \(GiB\)\. For more information about specifying the volume size, see [VolumeSize](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required: *Yes  
*Type*: Integer

`VolumeType`  
The volume type, such as `standard` or `io1`\. For more information about specifying the volume type, see [VolumeType](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EbsBlockDevice.html) for the `EbsBlockDevice` action in the *Amazon EC2 API Reference*\.  
*Required: *Yes  
*Type*: String