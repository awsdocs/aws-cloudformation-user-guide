# AWS::EC2::LaunchTemplate BlockDeviceMapping<a name="aws-properties-ec2-launchtemplate-blockdevicemapping"></a>

Information about a block device mapping for an Amazon EC2 launch template\.

 `BlockDeviceMapping` is a property of [ AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-syntax.json"></a>

```
{
  "[DeviceName](#cfn-ec2-launchtemplate-blockdevicemapping-devicename)" : String,
  "[Ebs](#cfn-ec2-launchtemplate-blockdevicemapping-ebs)" : Ebs,
  "[NoDevice](#cfn-ec2-launchtemplate-blockdevicemapping-nodevice)" : String,
  "[VirtualName](#cfn-ec2-launchtemplate-blockdevicemapping-virtualname)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-syntax.yaml"></a>

```
  [DeviceName](#cfn-ec2-launchtemplate-blockdevicemapping-devicename): String
  [Ebs](#cfn-ec2-launchtemplate-blockdevicemapping-ebs): 
    Ebs
  [NoDevice](#cfn-ec2-launchtemplate-blockdevicemapping-nodevice): String
  [VirtualName](#cfn-ec2-launchtemplate-blockdevicemapping-virtualname): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-blockdevicemapping-properties"></a>

`DeviceName`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-devicename"></a>
The device name \(for example, /dev/sdh or xvdh\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ebs`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-ebs"></a>
Parameters used to automatically set up EBS volumes when the instance is launched\.  
*Required*: No  
*Type*: [Ebs](aws-properties-ec2-launchtemplate-blockdevicemapping-ebs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoDevice`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-nodevice"></a>
Suppresses the specified device included in the block device mapping of the AMI\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualName`  <a name="cfn-ec2-launchtemplate-blockdevicemapping-virtualname"></a>
The virtual device name \(ephemeralN\)\. Instance store volumes are numbered starting from 0\. An instance type with 2 available instance store volumes can specify mappings for ephemeral0 and ephemeral1\. The number of available instance store volumes depends on the instance type\. After you connect to the instance, you must mount the volume\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-blockdevicemapping--seealso"></a>
+  [ LaunchTemplateBlockDeviceMappingRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateBlockDeviceMappingRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 

