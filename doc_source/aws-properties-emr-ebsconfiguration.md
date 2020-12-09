# AWS::EMR::InstanceGroupConfig EbsConfiguration<a name="aws-properties-emr-ebsconfiguration"></a>

The Amazon EBS configuration of a cluster instance\.

## Syntax<a name="aws-properties-emr-ebsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emr-ebsconfiguration-syntax.json"></a>

```
{
  "[EbsBlockDeviceConfigs](#cfn-emr-ebsconfiguration-ebsblockdeviceconfigs)" : [ EbsBlockDeviceConfig, ... ],
  "[EbsOptimized](#cfn-emr-ebsconfiguration-ebsoptimized)" : Boolean
}
```

### YAML<a name="aws-properties-emr-ebsconfiguration-syntax.yaml"></a>

```
  [EbsBlockDeviceConfigs](#cfn-emr-ebsconfiguration-ebsblockdeviceconfigs): 
    - EbsBlockDeviceConfig
  [EbsOptimized](#cfn-emr-ebsconfiguration-ebsoptimized): Boolean
```

## Properties<a name="aws-properties-emr-ebsconfiguration-properties"></a>

`EbsBlockDeviceConfigs`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfigs"></a>
An array of Amazon EBS volume specifications attached to a cluster instance\.  
*Required*: No  
*Type*: List of [EbsBlockDeviceConfig](aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EbsOptimized`  <a name="cfn-emr-ebsconfiguration-ebsoptimized"></a>
Indicates whether an Amazon EBS volume is EBS\-optimized\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)