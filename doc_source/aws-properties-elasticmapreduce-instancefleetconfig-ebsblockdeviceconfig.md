# AWS::EMR::InstanceFleetConfig EbsBlockDeviceConfig<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig"></a>

`EbsBlockDeviceConfig` is a subproperty of the `EbsConfiguration` property type\. `EbsBlockDeviceConfig` defines the number and type of EBS volumes to associate with all EC2 instances in an EMR cluster\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-syntax.json"></a>

```
{
  "[VolumeSpecification](#cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumespecification)" : VolumeSpecification,
  "[VolumesPerInstance](#cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumesperinstance)" : Integer
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-syntax.yaml"></a>

```
  [VolumeSpecification](#cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumespecification): 
    VolumeSpecification
  [VolumesPerInstance](#cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumesperinstance): Integer
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-properties"></a>

`VolumeSpecification`  <a name="cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumespecification"></a>
EBS volume specifications such as volume type, IOPS, and size \(GiB\) that will be requested for the EBS volume attached to an EC2 instance in the cluster\.  
*Required*: Yes  
*Type*: [VolumeSpecification](aws-properties-elasticmapreduce-instancefleetconfig-volumespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumesPerInstance`  <a name="cfn-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig-volumesperinstance"></a>
Number of EBS volumes with a specific volume configuration that will be associated with every instance in the instance group  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)