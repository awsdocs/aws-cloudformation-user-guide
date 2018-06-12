# Amazon Elastic Compute Cloud SpotFleet BlockDeviceMappings<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings"></a>

`BlockDeviceMappings` is a property of the [Amazon Elastic Compute Cloud SpotFleet LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md) property that defines the block devices that are mapped to an instance\.

## Syntax<a name="w3ab2c21c14d778b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-syntax.json"></a>

```
{
  "[DeviceName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-devicename)" : String,
  "[Ebs](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs)" : EBSBlockDevice,
  "[NoDevice](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-nodevice)" : Boolean,
  "[VirtualName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-virtualname)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-syntax.yaml"></a>

```
[DeviceName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-devicename): String
[Ebs](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs):
  EBSBlockDevice
[NoDevice](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-nodevice): Boolean
[VirtualName](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-virtualname): String
```

## Properties<a name="w3ab2c21c14d778b7"></a>

`DeviceName`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-devicename"></a>
The name of the device within the EC2 instance, such as `/dev/dsh` or `xvdh`\.  
*Required*: Yes  
*Type*: String

`Ebs`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs"></a>
The Amazon Elastic Block Store \(Amazon EBS\) volume information\.  
*Required*: Conditional You can specify either the `VirtualName` or `Ebs`, but not both\.  
*Type*: [Amazon Elastic Compute Cloud SpotFleet Ebs](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs.md)

`NoDevice`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-nodevice"></a>
Suppresses the specified device that is included in the block device mapping of the Amazon Machine Image \(AMI\)\.  
*Required*: No  
*Type*: Boolean

`VirtualName`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-virtualname"></a>
The name of the virtual device\. The name must be in the form `ephemeralX` where *X* is a number equal to or greater than zero \(0\), for example, `ephemeral0`\.  
*Required*: Conditional You can specify either the `VirtualName` or `Ebs`, but not both\.  
*Type*: String