# Amazon EMR EbsConfiguration<a name="aws-properties-emr-ebsconfiguration"></a>

`EbsConfiguration` is a property of the [Amazon EMR Cluster InstanceGroupConfig](aws-properties-emr-cluster-jobflowinstancesconfig-instancegroupconfig.md) property and the [AWS::EMR::InstanceGroupConfig](aws-resource-emr-instancegroupconfig.md) resource that defines Amazon Elastic Block Store \(Amazon EBS\) storage volumes to attach to your Amazon EMR \(Amazon EMR\) instances\.

## Syntax<a name="w3ab2c21c14e1145b5"></a>

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

## Properties<a name="w3ab2c21c14e1145b7"></a>

`EbsBlockDeviceConfigs`  <a name="cfn-emr-ebsconfiguration-ebsblockdeviceconfigs"></a>
Configures the block storage devices that are associated with your EMR instances\.  
*Required*: No  
*Type*: List of [Amazon EMR EbsConfiguration EbsBlockDeviceConfigs](aws-properties-emr-ebsconfiguration-ebsblockdeviceconfig.md)

`EbsOptimized`  <a name="cfn-emr-ebsconfiguration-ebsoptimized"></a>
Indicates whether the instances are optimized for Amazon EBS I/O\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal EBS I/O performance\. For more information about fees and supported instance types, see [EBS\-Optimized Instances](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSOptimized.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: Boolean  
*Default value*: `false`