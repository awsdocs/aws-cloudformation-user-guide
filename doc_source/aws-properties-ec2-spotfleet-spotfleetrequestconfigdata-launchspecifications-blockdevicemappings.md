# Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications BlockDeviceMappings<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings"></a>

`BlockDeviceMappings` is a property of the [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md) property that defines the block devices that are mapped to an instance\.

## Syntax<a name="w3ab2c21c14d618b5"></a>

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-devicename)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs)" : EBSBlockDevice,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-nodevice)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-virtualname)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-devicename): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs):
  EBSBlockDevice
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-nodevice): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-virtualname): String
```

## Properties<a name="w3ab2c21c14d618b7"></a>

`DeviceName`  
The name of the device within the EC2 instance, such as `/dev/dsh` or `xvdh`\.  
*Required: *Yes  
*Type*: String

`Ebs`  
The Amazon Elastic Block Store \(Amazon EBS\) volume information\.  
*Required: *Conditional You can specify either the `VirtualName` or `Ebs`, but not both\.  
*Type*: [Amazon Elastic Compute Cloud SpotFleet SpotFleetRequestConfigData LaunchSpecifications BlockDeviceMappings Ebs](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-blockdevicemappings-ebs.md)

`NoDevice`  
Suppresses the specified device that is included in the block device mapping of the Amazon Machine Image \(AMI\)\.  
*Required: *No  
*Type*: Boolean

`VirtualName`  
The name of the virtual device\. The name must be in the form `ephemeralX` where *X* is a number equal to or greater than zero \(0\), for example, `ephemeral0`\.  
*Required: *Conditional You can specify either the `VirtualName` or `Ebs`, but not both\.  
*Type*: String