# AWS::EC2::Instance BlockDeviceMapping<a name="aws-properties-ec2-blockdev-mapping"></a>

Specifies a block device mapping for an instance\.

 `BlockDeviceMapping` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

## Syntax<a name="aws-properties-ec2-blockdev-mapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-blockdev-mapping-syntax.json"></a>

```
{
  "[DeviceName](#cfn-ec2-blockdev-mapping-devicename)" : String,
  "[Ebs](#cfn-ec2-blockdev-mapping-ebs)" : Ebs,
  "[NoDevice](#cfn-ec2-blockdev-mapping-nodevice)" : NoDevice,
  "[VirtualName](#cfn-ec2-blockdev-mapping-virtualname)" : String
}
```

### YAML<a name="aws-properties-ec2-blockdev-mapping-syntax.yaml"></a>

```
  [DeviceName](#cfn-ec2-blockdev-mapping-devicename): String
  [Ebs](#cfn-ec2-blockdev-mapping-ebs): 
    Ebs
  [NoDevice](#cfn-ec2-blockdev-mapping-nodevice): 
    NoDevice
  [VirtualName](#cfn-ec2-blockdev-mapping-virtualname): String
```

## Properties<a name="aws-properties-ec2-blockdev-mapping-properties"></a>

`DeviceName`  <a name="cfn-ec2-blockdev-mapping-devicename"></a>
The device name \(for example, `/dev/sdh` or `xvdh`\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ebs`  <a name="cfn-ec2-blockdev-mapping-ebs"></a>
Parameters used to automatically set up EBS volumes when the instance is launched\.  
You can specify either `VirtualName` or `Ebs`, but not both\.  
*Required*: Conditional  
*Type*: [Ebs](aws-properties-ec2-blockdev-template.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoDevice`  <a name="cfn-ec2-blockdev-mapping-nodevice"></a>
Suppresses the specified device included in the block device mapping of the AMI\.  
*Required*: No  
*Type*: [NoDevice](aws-properties-ec2-instance-nodevice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualName`  <a name="cfn-ec2-blockdev-mapping-virtualname"></a>
The virtual device name \(`ephemeral`N\)\. The name must be in the form `ephemeral`*X* where *X* is a number starting from zero \(0\)\. For example, an instance type with 2 available instance store volumes can specify mappings for `ephemeral0` and `ephemeral1`\. The number of available instance store volumes depends on the instance type\. After you connect to the instance, you must mount the volume\.  
NVMe instance store volumes are automatically enumerated and assigned a device name\. Including them in your block device mapping has no effect\.  
You can specify either `VirtualName` or `Ebs`, but not both\.  
 *Constraints*: For M3 instances, you must specify instance store volumes in the block device mapping for the instance\. When you launch an M3 instance, we ignore any instance store volumes specified in the block device mapping for the AMI\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-ec2-blockdev-mapping--examples"></a>

### Block Device Mapping with two EBS Volumes<a name="aws-properties-ec2-blockdev-mapping--examples--Block_Device_Mapping_with_two_EBS_Volumes"></a>

This example sets the EBS\-backed root device \(/dev/sda1\) size to 50 GiB, and another EBS\-backed device mapped to /dev/sdm that is 100 GiB in size\.

#### JSON<a name="aws-properties-ec2-blockdev-mapping--examples--Block_Device_Mapping_with_two_EBS_Volumes--json"></a>

```
"BlockDeviceMappings" : [
   {
      "DeviceName" : "/dev/sda1",
      "Ebs" : { "VolumeSize" : "50" }
   },
   {
      "DeviceName" : "/dev/sdm",
      "Ebs" : { "VolumeSize" : "100" }
   }
]
```

#### YAML<a name="aws-properties-ec2-blockdev-mapping--examples--Block_Device_Mapping_with_two_EBS_Volumes--yaml"></a>

```
BlockDeviceMappings:
  - DeviceName: /dev/sda1
    Ebs:
      VolumeSize: 50
  - DeviceName: /dev/sdm
    Ebs:
      VolumeSize: 100
```

### Block Device Mapping with an Ephemeral Drive<a name="aws-properties-ec2-blockdev-mapping--examples--Block_Device_Mapping_with_an_Ephemeral_Drive"></a>

This example maps an ephemeral drive to device /dev/sdc\.

#### JSON<a name="aws-properties-ec2-blockdev-mapping--examples--Block_Device_Mapping_with_an_Ephemeral_Drive--json"></a>

```
"BlockDeviceMappings" : [
   {
      "DeviceName"  : "/dev/sdc",
      "VirtualName" : "ephemeral0"
   }
]
```

#### YAML<a name="aws-properties-ec2-blockdev-mapping--examples--Block_Device_Mapping_with_an_Ephemeral_Drive--yaml"></a>

```
BlockDeviceMappings:
  - DeviceName: /dev/sdc
    VirtualName: ephemeral0
```

### Unmapping an AMI\-defined Device<a name="aws-properties-ec2-blockdev-mapping--examples--Unmapping_an_AMI-defined_Device"></a>

To unmap a device defined in the AMI, set the `NoDevice` property to an empty map, as shown here:

#### JSON<a name="aws-properties-ec2-blockdev-mapping--examples--Unmapping_an_AMI-defined_Device--json"></a>

```
"BlockDeviceMappings" : [
   {
      "DeviceName":"/dev/sde",
      "NoDevice": {}
   }
]
```

#### YAML<a name="aws-properties-ec2-blockdev-mapping--examples--Unmapping_an_AMI-defined_Device--yaml"></a>

```
BlockDeviceMappings:
  - DeviceName: /dev/sde
    NoDevice: {}
```

## See also<a name="aws-properties-ec2-blockdev-mapping--seealso"></a>
+  [ Amazon EC2 Instance Store](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) in the *Amazon Elastic Compute Cloud User Guide*\.