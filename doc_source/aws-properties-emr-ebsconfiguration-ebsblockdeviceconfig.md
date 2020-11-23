# AWS::EMR::InstanceGroupConfig EbsBlockDeviceConfig<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig"></a>

Configuration of requested EBS block device associated with the instance group with count of volumes that will be associated to every instance\.

## Syntax<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-properties"></a>

`VolumeSpecification`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification"></a>
EBS volume specifications such as volume type, IOPS, and size \(GiB\) that will be requested for the EBS volume attached to an EC2 instance in the cluster\.  
*Required*: Yes  
*Type*: [VolumeSpecification](aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig-volumespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumesPerInstance`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfig-volumesperinstance"></a>
Number of EBS volumes with a specific volume configuration that will be associated with every instance in the instance group  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)