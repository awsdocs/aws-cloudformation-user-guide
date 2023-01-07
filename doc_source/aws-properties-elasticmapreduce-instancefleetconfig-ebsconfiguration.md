# AWS::EMR::InstanceFleetConfig EbsConfiguration<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsconfiguration"></a>

`EbsConfiguration` determines the EBS volumes to attach to EMR cluster instances\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsconfiguration-syntax.json"></a>

```
{
  "[EbsBlockDeviceConfigs](#cfn-elasticmapreduce-instancefleetconfig-ebsconfiguration-ebsblockdeviceconfigs)" : [ EbsBlockDeviceConfig, ... ],
  "[EbsOptimized](#cfn-elasticmapreduce-instancefleetconfig-ebsconfiguration-ebsoptimized)" : Boolean
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsconfiguration-syntax.yaml"></a>

```
  [EbsBlockDeviceConfigs](#cfn-elasticmapreduce-instancefleetconfig-ebsconfiguration-ebsblockdeviceconfigs): 
    - EbsBlockDeviceConfig
  [EbsOptimized](#cfn-elasticmapreduce-instancefleetconfig-ebsconfiguration-ebsoptimized): Boolean
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-ebsconfiguration-properties"></a>

`EbsBlockDeviceConfigs`  <a name="cfn-elasticmapreduce-instancefleetconfig-ebsconfiguration-ebsblockdeviceconfigs"></a>
An array of Amazon EBS volume specifications attached to a cluster instance\.  
*Required*: No  
*Type*: List of [EbsBlockDeviceConfig](aws-properties-elasticmapreduce-instancefleetconfig-ebsblockdeviceconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsOptimized`  <a name="cfn-elasticmapreduce-instancefleetconfig-ebsconfiguration-ebsoptimized"></a>
Indicates whether an Amazon EBS volume is EBS\-optimized\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)