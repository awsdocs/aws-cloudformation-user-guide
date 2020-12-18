# AWS::EMR::Cluster EbsConfiguration<a name="aws-properties-elasticmapreduce-cluster-ebsconfiguration"></a>

`EbsConfiguration` is a subproperty of `InstanceFleetConfig` or `InstanceGroupConfig`\. `EbsConfiguration` determines the EBS volumes to attach to EMR cluster instances\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-ebsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-ebsconfiguration-syntax.json"></a>

```
{
  "[EbsBlockDeviceConfigs](#cfn-elasticmapreduce-cluster-ebsconfiguration-ebsblockdeviceconfigs)" : [ EbsBlockDeviceConfig, ... ],
  "[EbsOptimized](#cfn-elasticmapreduce-cluster-ebsconfiguration-ebsoptimized)" : Boolean
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-ebsconfiguration-syntax.yaml"></a>

```
  [EbsBlockDeviceConfigs](#cfn-elasticmapreduce-cluster-ebsconfiguration-ebsblockdeviceconfigs): 
    - EbsBlockDeviceConfig
  [EbsOptimized](#cfn-elasticmapreduce-cluster-ebsconfiguration-ebsoptimized): Boolean
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-ebsconfiguration-properties"></a>

`EbsBlockDeviceConfigs`  <a name="cfn-elasticmapreduce-cluster-ebsconfiguration-ebsblockdeviceconfigs"></a>
An array of Amazon EBS volume specifications attached to a cluster instance\.  
*Required*: No  
*Type*: List of [EbsBlockDeviceConfig](aws-properties-elasticmapreduce-cluster-ebsblockdeviceconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EbsOptimized`  <a name="cfn-elasticmapreduce-cluster-ebsconfiguration-ebsoptimized"></a>
Indicates whether an Amazon EBS volume is EBS\-optimized\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)