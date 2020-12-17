# AWS::OpsWorks::Instance BlockDeviceMapping<a name="aws-properties-opsworks-instance-blockdevicemapping"></a>

Describes a block device mapping\. This data type maps directly to the Amazon EC2 [BlockDeviceMapping](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_BlockDeviceMapping.html) data type\. 

## Syntax<a name="aws-properties-opsworks-instance-blockdevicemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-instance-blockdevicemapping-syntax.json"></a>

```
{
  "[DeviceName](#cfn-opsworks-instance-blockdevicemapping-devicename)" : String,
  "[Ebs](#cfn-opsworks-instance-blockdevicemapping-ebs)" : EbsBlockDevice,
  "[NoDevice](#cfn-opsworks-instance-blockdevicemapping-nodevice)" : String,
  "[VirtualName](#cfn-opsworks-instance-blockdevicemapping-virtualname)" : String
}
```

### YAML<a name="aws-properties-opsworks-instance-blockdevicemapping-syntax.yaml"></a>

```
  [DeviceName](#cfn-opsworks-instance-blockdevicemapping-devicename): String
  [Ebs](#cfn-opsworks-instance-blockdevicemapping-ebs): 
    EbsBlockDevice
  [NoDevice](#cfn-opsworks-instance-blockdevicemapping-nodevice): String
  [VirtualName](#cfn-opsworks-instance-blockdevicemapping-virtualname): String
```

## Properties<a name="aws-properties-opsworks-instance-blockdevicemapping-properties"></a>

`DeviceName`  <a name="cfn-opsworks-instance-blockdevicemapping-devicename"></a>
The device name that is exposed to the instance, such as `/dev/sdh`\. For the root device, you can use the explicit device name or you can set this parameter to `ROOT_DEVICE` and AWS OpsWorks Stacks will provide the correct device name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ebs`  <a name="cfn-opsworks-instance-blockdevicemapping-ebs"></a>
An `EBSBlockDevice` that defines how to configure an Amazon EBS volume when the instance is launched\. You can specify either the `VirtualName` or Ebs, but not both\.  
*Required*: Conditional  
*Type*: [EbsBlockDevice](aws-properties-opsworks-instance-ebsblockdevice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoDevice`  <a name="cfn-opsworks-instance-blockdevicemapping-nodevice"></a>
Suppresses the specified device included in the AMI's block device mapping\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualName`  <a name="cfn-opsworks-instance-blockdevicemapping-virtualname"></a>
The virtual device name\. For more information, see [BlockDeviceMapping](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_BlockDeviceMapping.html)\. You can specify either the `VirtualName` or Ebs, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)