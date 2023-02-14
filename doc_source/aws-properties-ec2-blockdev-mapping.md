# AWS::EC2::Instance BlockDeviceMapping<a name="aws-properties-ec2-blockdev-mapping"></a>

Specifies a block device mapping for an instance\. You must specify exactly one of the following properties: `VirtualName`, `Ebs`, or `NoDevice`\.

`BlockDeviceMapping` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

**Important**  
After the instance is running, you can modify only the `DeleteOnTermination` parameter for the attached volumes without interrupting the instance\. Modifying any other parameter results in instance [ replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)\.

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
After the instance is running, this parameter is used to specify the device name of the block device mapping to update\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ebs`  <a name="cfn-ec2-blockdev-mapping-ebs"></a>
Parameters used to automatically set up EBS volumes when the instance is launched\.  
After the instance is running, you can modify only the `DeleteOnTermination` parameter for the attached volumes without interrupting the instance\. Modifying any other parameter results in instance [ replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)\.
*Required*: Conditional  
*Type*: [Ebs](aws-properties-ec2-blockdev-template.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoDevice`  <a name="cfn-ec2-blockdev-mapping-nodevice"></a>
To omit the device from the block device mapping, specify an empty string\.  
After the instance is running, modifying this parameter results in instance [ replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)\.
*Required*: Conditional  
*Type*: [NoDevice](aws-properties-ec2-instance-nodevice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualName`  <a name="cfn-ec2-blockdev-mapping-virtualname"></a>
The virtual device name \(`ephemeral`N\)\. The name must be in the form `ephemeral`*X* where *X* is a number starting from zero \(0\)\. For example, an instance type with 2 available instance store volumes can specify mappings for `ephemeral0` and `ephemeral1`\. The number of available instance store volumes depends on the instance type\. After you connect to the instance, you must mount the volume\.  
NVMe instance store volumes are automatically enumerated and assigned a device name\. Including them in your block device mapping has no effect\.  
 *Constraints*: For M3 instances, you must specify instance store volumes in the block device mapping for the instance\. When you launch an M3 instance, we ignore any instance store volumes specified in the block device mapping for the AMI\.  
After the instance is running, modifying this parameter results in instance [ replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)\.
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-ec2-blockdev-mapping--examples"></a>

### Block device mapping with two EBS volumes<a name="aws-properties-ec2-blockdev-mapping--examples--Block_device_mapping_with_two_EBS_volumes"></a>

This example sets the EBS\-backed root device \(/dev/sda1\) size to 50 GiB, and another EBS\-backed device mapped to /dev/sdm that is 100 GiB in size\.

#### JSON<a name="aws-properties-ec2-blockdev-mapping--examples--Block_device_mapping_with_two_EBS_volumes--json"></a>

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

#### YAML<a name="aws-properties-ec2-blockdev-mapping--examples--Block_device_mapping_with_two_EBS_volumes--yaml"></a>

```
BlockDeviceMappings:
  - DeviceName: /dev/sda1
    Ebs:
      VolumeSize: 50
  - DeviceName: /dev/sdm
    Ebs:
      VolumeSize: 100
```

### Block device mapping with an instance store volume<a name="aws-properties-ec2-blockdev-mapping--examples--Block_device_mapping_with_an_instance_store_volume"></a>

This example maps an instance store volume to device /dev/sdc\.

#### JSON<a name="aws-properties-ec2-blockdev-mapping--examples--Block_device_mapping_with_an_instance_store_volume--json"></a>

```
"BlockDeviceMappings" : [
   {
      "DeviceName"  : "/dev/sdc",
      "VirtualName" : "ephemeral0"
   }
]
```

#### YAML<a name="aws-properties-ec2-blockdev-mapping--examples--Block_device_mapping_with_an_instance_store_volume--yaml"></a>

```
BlockDeviceMappings:
  - DeviceName: /dev/sdc
    VirtualName: ephemeral0
```

### Unmap an AMI\-defined device<a name="aws-properties-ec2-blockdev-mapping--examples--Unmap_an_AMI-defined_device"></a>

To unmap a device defined in the AMI, set the `NoDevice` property to an empty map, as shown here:

#### JSON<a name="aws-properties-ec2-blockdev-mapping--examples--Unmap_an_AMI-defined_device--json"></a>

```
"BlockDeviceMappings" : [
   {
      "DeviceName":"/dev/sde",
      "NoDevice": {}
   }
]
```

#### YAML<a name="aws-properties-ec2-blockdev-mapping--examples--Unmap_an_AMI-defined_device--yaml"></a>

```
BlockDeviceMappings:
  - DeviceName: /dev/sde
    NoDevice: {}
```

## See also<a name="aws-properties-ec2-blockdev-mapping--seealso"></a>
+  [ Amazon EC2 instance store](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) in the *Amazon EC2 User Guide*\.