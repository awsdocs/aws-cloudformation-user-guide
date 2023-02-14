# AWS::Lightsail::Instance Disk<a name="aws-properties-lightsail-instance-disk"></a>

`Disk` is a property of the [Hardware](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lightsail-instance-hardware.html) property\. It describes a disk attached to an instance\.

## Syntax<a name="aws-properties-lightsail-instance-disk-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-instance-disk-syntax.json"></a>

```
{
  "[AttachedTo](#cfn-lightsail-instance-disk-attachedto)" : String,
  "[AttachmentState](#cfn-lightsail-instance-disk-attachmentstate)" : String,
  "[DiskName](#cfn-lightsail-instance-disk-diskname)" : String,
  "[IOPS](#cfn-lightsail-instance-disk-iops)" : Integer,
  "[IsSystemDisk](#cfn-lightsail-instance-disk-issystemdisk)" : Boolean,
  "[Path](#cfn-lightsail-instance-disk-path)" : String,
  "[SizeInGb](#cfn-lightsail-instance-disk-sizeingb)" : String
}
```

### YAML<a name="aws-properties-lightsail-instance-disk-syntax.yaml"></a>

```
  [AttachedTo](#cfn-lightsail-instance-disk-attachedto): String
  [AttachmentState](#cfn-lightsail-instance-disk-attachmentstate): String
  [DiskName](#cfn-lightsail-instance-disk-diskname): String
  [IOPS](#cfn-lightsail-instance-disk-iops): Integer
  [IsSystemDisk](#cfn-lightsail-instance-disk-issystemdisk): Boolean
  [Path](#cfn-lightsail-instance-disk-path): String
  [SizeInGb](#cfn-lightsail-instance-disk-sizeingb): String
```

## Properties<a name="aws-properties-lightsail-instance-disk-properties"></a>

`AttachedTo`  <a name="cfn-lightsail-instance-disk-attachedto"></a>
The resources to which the disk is attached\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`AttachmentState`  <a name="cfn-lightsail-instance-disk-attachmentstate"></a>
\(Deprecated\) The attachment state of the disk\.  
In releases prior to November 14, 2017, this parameter returned `attached` for system disks in the API response\. It is now deprecated, but still included in the response\. Use `isAttached` instead\.
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`DiskName`  <a name="cfn-lightsail-instance-disk-diskname"></a>
The unique name of the disk\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IOPS`  <a name="cfn-lightsail-instance-disk-iops"></a>
The input/output operations per second \(IOPS\) of the disk\.  
*Required*: No  
*Type*: Integer  
*Update requires*: Updates are not supported\.

`IsSystemDisk`  <a name="cfn-lightsail-instance-disk-issystemdisk"></a>
A Boolean value indicating whether this disk is a system disk \(has an operating system loaded on it\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: Updates are not supported\.

`Path`  <a name="cfn-lightsail-instance-disk-path"></a>
The disk path\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`SizeInGb`  <a name="cfn-lightsail-instance-disk-sizeingb"></a>
The size of the disk in GB\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.