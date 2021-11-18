# AWS::Lightsail::Instance Hardware<a name="aws-properties-lightsail-instance-hardware"></a>

`Hardware` is a property of the [AWS::Lightsail::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-instance.html) resource\. It describes the hardware properties for the instance, such as the vCPU count, attached disks, and amount of RAM\.

## Syntax<a name="aws-properties-lightsail-instance-hardware-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-instance-hardware-syntax.json"></a>

```
{
  "[CpuCount](#cfn-lightsail-instance-hardware-cpucount)" : Integer,
  "[Disks](#cfn-lightsail-instance-hardware-disks)" : [ Disk, ... ],
  "[RamSizeInGb](#cfn-lightsail-instance-hardware-ramsizeingb)" : Integer
}
```

### YAML<a name="aws-properties-lightsail-instance-hardware-syntax.yaml"></a>

```
  [CpuCount](#cfn-lightsail-instance-hardware-cpucount): Integer
  [Disks](#cfn-lightsail-instance-hardware-disks): 
    - Disk
  [RamSizeInGb](#cfn-lightsail-instance-hardware-ramsizeingb): Integer
```

## Properties<a name="aws-properties-lightsail-instance-hardware-properties"></a>

`CpuCount`  <a name="cfn-lightsail-instance-hardware-cpucount"></a>
The number of vCPUs the instance has\.  
The `CpuCount` property is read\-only and should not be specified in a create instance or update instance request\.
*Required*: No  
*Type*: Integer  
*Update requires*: Updates are not supported\.

`Disks`  <a name="cfn-lightsail-instance-hardware-disks"></a>
The disks attached to the instance\.  
The instance restarts when performing an attach disk or detach disk request\. This resets the public IP address of your instance if a static IP isn't attached to it\.  
*Required*: No  
*Type*: List of [Disk](aws-properties-lightsail-instance-disk.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`RamSizeInGb`  <a name="cfn-lightsail-instance-hardware-ramsizeingb"></a>
The amount of RAM in GB on the instance \(for example, `1.0`\)\.  
The `RamSizeInGb` property is read\-only and should not be specified in a create instance or update instance request\.
*Required*: No  
*Type*: Integer  
*Update requires*: Updates are not supported\.