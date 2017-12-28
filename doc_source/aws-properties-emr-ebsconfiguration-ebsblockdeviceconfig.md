# Amazon EMR EbsConfiguration EbsBlockDeviceConfigs<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig"></a>

`EbsBlockDeviceConfigs` is a property of the [Amazon EMR EbsConfiguration](aws-properties-emr-ebsconfiguration.md) property that defines the settings for the Amazon Elastic Block Store \(Amazon EBS\) volumes that Amazon EMR \(Amazon EMR\) associates with your instances\.

## Syntax<a name="w3ab2c21c14d958b5"></a>

### JSON<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification)" : VolumeSpecification,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumesperinstance)" : Integer
}
```

### YAML<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification):
  VolumeSpecification
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumesperinstance): Integer
```

## Properties<a name="w3ab2c21c14d958b7"></a>

`VolumeSpecification`  
The settings for the Amazon EBS volumes\.  
*Required: *Yes  
*Type*: [Amazon EMR EbsConfiguration EbsBlockDeviceConfig VolumeSpecification](aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification.md)

`VolumesPerInstance`  
The number of Amazon EBS volumes that you want to create for each instance in the EMR cluster or instance group\. The number cannot be 0\.  
*Required: *No  
*Type*: Integer