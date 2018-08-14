# Amazon EMR EbsConfiguration EbsBlockDeviceConfigs<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig"></a>

`EbsBlockDeviceConfigs` is a property of the [Amazon EMR EbsConfiguration](aws-properties-emr-ebsconfiguration.md) property that defines the settings for the Amazon Elastic Block Store \(Amazon EBS\) volumes that Amazon EMR \(Amazon EMR\) associates with your instances\.

## Syntax<a name="w3ab2c21c14e1149b5"></a>

### JSON<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-syntax.json"></a>

```
{
  "[VolumeSpecification](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification)" : VolumeSpecification,
  "[VolumesPerInstance](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumesperinstance)" : Integer
}
```

### YAML<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-syntax.yaml"></a>

```
[VolumeSpecification](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification):
  VolumeSpecification
[VolumesPerInstance](#cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumesperinstance): Integer
```

## Properties<a name="w3ab2c21c14e1149b7"></a>

`VolumeSpecification`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification"></a>
The settings for the Amazon EBS volumes\.  
*Required*: Yes  
*Type*: [Amazon EMR EbsConfiguration EbsBlockDeviceConfig VolumeSpecification](aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification.md)

`VolumesPerInstance`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumesperinstance"></a>
The number of Amazon EBS volumes that you want to create for each instance in the EMR cluster or instance group\. The number cannot be 0\.  
*Required*: No  
*Type*: Integer