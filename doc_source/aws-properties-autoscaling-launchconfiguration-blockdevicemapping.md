# AWS::AutoScaling::LaunchConfiguration BlockDeviceMapping<a name="aws-properties-autoscaling-launchconfiguration-blockdevicemapping"></a>

 `BlockDeviceMapping` specifies a block device mapping for the `BlockDeviceMappings` property of the [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) resource\.

Each instance that is launched has an associated root device volume, either an Amazon EBS volume or an instance store volume\. You can use block device mappings to specify additional EBS volumes or instance store volumes to attach to an instance when it is launched\. 

For more information, see [Example block device mapping](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/block-device-mapping-concepts.html#block-device-mapping-ex) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-properties-autoscaling-launchconfiguration-blockdevicemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-launchconfiguration-blockdevicemapping-syntax.json"></a>

```
{
  "[DeviceName](#cfn-autoscaling-launchconfiguration-blockdevicemapping-devicename)" : String,
  "[Ebs](#cfn-autoscaling-launchconfiguration-blockdevicemapping-ebs)" : BlockDevice,
  "[NoDevice](#cfn-autoscaling-launchconfiguration-blockdevicemapping-nodevice)" : Boolean,
  "[VirtualName](#cfn-autoscaling-launchconfiguration-blockdevicemapping-virtualname)" : String
}
```

### YAML<a name="aws-properties-autoscaling-launchconfiguration-blockdevicemapping-syntax.yaml"></a>

```
  [DeviceName](#cfn-autoscaling-launchconfiguration-blockdevicemapping-devicename): String
  [Ebs](#cfn-autoscaling-launchconfiguration-blockdevicemapping-ebs): 
    BlockDevice
  [NoDevice](#cfn-autoscaling-launchconfiguration-blockdevicemapping-nodevice): Boolean
  [VirtualName](#cfn-autoscaling-launchconfiguration-blockdevicemapping-virtualname): String
```

## Properties<a name="aws-properties-autoscaling-launchconfiguration-blockdevicemapping-properties"></a>

`DeviceName`  <a name="cfn-autoscaling-launchconfiguration-blockdevicemapping-devicename"></a>
The device name assigned to the volume \(for example, `/dev/sdh` or `xvdh`\)\. For more information, see [Device naming on Linux instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/device_naming.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
To define a block device mapping, set the device name and exactly one of the following properties: `Ebs`, `NoDevice`, or `VirtualName`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ebs`  <a name="cfn-autoscaling-launchconfiguration-blockdevicemapping-ebs"></a>
Information to attach an EBS volume to an instance at launch\.  
*Required*: No  
*Type*: [BlockDevice](aws-properties-autoscaling-launchconfiguration-blockdevice.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NoDevice`  <a name="cfn-autoscaling-launchconfiguration-blockdevicemapping-nodevice"></a>
Setting this value to `true` prevents a volume that is included in the block device mapping of the AMI from being mapped to the specified device name at launch\.  
If `NoDevice` is `true` for the root device, instances might fail the EC2 health check\. In that case, Amazon EC2 Auto Scaling launches replacement instances\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VirtualName`  <a name="cfn-autoscaling-launchconfiguration-blockdevicemapping-virtualname"></a>
The name of the instance store volume \(virtual device\) to attach to an instance at launch\. The name must be in the form ephemeral*X* where *X* is a number starting from zero \(0\), for example, `ephemeral0`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-autoscaling-launchconfiguration-blockdevicemapping--seealso"></a>
+ [Amazon EC2 instance store](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) in the *Amazon EC2 User Guide for Linux Instances*
+ [Amazon Elastic Block Store \(Amazon EBS\)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html) in the *Amazon EC2 User Guide for Linux Instances*

