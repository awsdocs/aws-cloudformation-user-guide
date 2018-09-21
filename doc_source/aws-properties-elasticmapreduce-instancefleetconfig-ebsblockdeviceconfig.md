# Amazon EMR InstanceFleetConfig EbsBlockDeviceConfig<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig"></a>

Use the `EbsBlockDeviceConfig` property to specify the settings for the Amazon EBS volumes that Amazon EMR associates with your instances\. The `EbsBlockDeviceConfigs` subproperty of the [Amazon EMR InstanceFleetConfig EbsConfiguration](aws-properties-elasticmapreduce-instancefleetconfig-ebsconfiguration.md) property contains a list of `EbsBlockDeviceConfig` property types\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-syntax.json"></a>

```
{
  "[VolumeSpecification](#cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumespecification)" : [*VolumeSpecification*](aws-properties-elasticmapreduce-instancefleetconfig-volumespecification.md),
  "[VolumesPerInstance](#cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumesperinstance)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-syntax.yaml"></a>

```
[VolumeSpecification](#cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumespecification):
  [*VolumeSpecification*](aws-properties-elasticmapreduce-instancefleetconfig-volumespecification.md)
[VolumesPerInstance](#cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumesperinstance): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-properties"></a>

`VolumeSpecification`  <a name="cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumespecification"></a>
Amazon EBS volume specifications, such as volume type, IOPS, and size \(GiB\), for the EBS volume attached to an EC2 instance in the fleet\.  
*Required*: Yes  
*Type*: [Amazon EMR InstanceFleetConfig VolumeSpecification](aws-properties-elasticmapreduce-instancefleetconfig-volumespecification.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VolumesPerInstance`  <a name="cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumesperinstance"></a>
The number of Amazon EBS volumes with a specific volume configuration that are associated with every instance in the fleet\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)