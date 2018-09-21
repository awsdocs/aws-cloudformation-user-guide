# AWS OpsWorks Instance BlockDeviceMapping<a name="aws-properties-opsworks-instance-blockdevicemapping"></a>

`BlockDeviceMappings` is a property of the [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md) resource that defines the block devices that are mapped to an AWS OpsWorks instance\.

## Syntax<a name="aws-properties-opsworks-instance-blockdevicemapping-syntax"></a>

### JSON<a name="aws-properties-opsworks-instance-blockdevicemapping-syntax.json"></a>

```
{
  "[DeviceName](#cfn-opsworks-instance-blockdevicemapping-devicename)" : String,
  "[Ebs](#cfn-opsworks-instance-blockdevicemapping-ebs)" : [EbsBlockDevice](aws-properties-opsworks-instance-blockdevicemapping-ebsblockdevice.md),
  "[NoDevice](#cfn-opsworks-instance-blockdevicemapping-nodevice)" : String,
  "[VirtualName](#cfn-opsworks-instance-blockdevicemapping-virtualname)" : String
}
```

### YAML<a name="aws-properties-opsworks-instance-blockdevicemapping-syntax.yaml"></a>

```
[DeviceName](#cfn-opsworks-instance-blockdevicemapping-devicename): String
[Ebs](#cfn-opsworks-instance-blockdevicemapping-ebs):
[EbsBlockDevice](aws-properties-opsworks-instance-blockdevicemapping-ebsblockdevice.md)
[NoDevice](#cfn-opsworks-instance-blockdevicemapping-nodevice): String
[VirtualName](#cfn-opsworks-instance-blockdevicemapping-virtualname): String
```

## Properties<a name="aws-properties-opsworks-instance-blockdevicemapping-properties"></a>

`DeviceName`  <a name="cfn-opsworks-instance-blockdevicemapping-devicename"></a>
The name of the device that is exposed to the instance, such as `/dev/dsh` or `xvdh`\. For the root device, you can use the explicit device name or you can set this parameter to `ROOT_DEVICE`\. If you set the parameter to `ROOT_DEVICE`, AWS OpsWorks provides the correct device name\.  
*Required*: No  
*Type*: String

`Ebs`  <a name="cfn-opsworks-instance-blockdevicemapping-ebs"></a>
Configuration information about the Amazon Elastic Block Store \(Amazon EBS\) volume\.  
*Required*: Conditional You can specify either the `VirtualName` or `Ebs`, but not both\.  
*Type*: [AWS OpsWorks Instance BlockDeviceMapping EbsBlockDevice](aws-properties-opsworks-instance-blockdevicemapping-ebsblockdevice.md)

`NoDevice`  <a name="cfn-opsworks-instance-blockdevicemapping-nodevice"></a>
Suppresses the device that is specified in the block device mapping of the AWS OpsWorks instance Amazon Machine Image \(AMI\)\.  
*Required*: No  
*Type*: String

`VirtualName`  <a name="cfn-opsworks-instance-blockdevicemapping-virtualname"></a>
The name of the virtual device\. The name must be in the form `ephemeralX`, where *X* is a number equal to or greater than zero \(0\), for example, `ephemeral0`\.  
*Required*: Conditional You can specify either the `VirtualName` or `Ebs`, but not both\.  
*Type*: String