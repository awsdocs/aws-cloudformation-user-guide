# Amazon EC2 Auto Scaling LaunchConfiguration BlockDeviceMapping<a name="aws-properties-as-launchconfig-blockdev-mapping"></a>

The Amazon EC2 Auto Scaling `BlockDeviceMapping` type is an embedded property of the [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md) type\.

## Syntax<a name="w2922ab1c21c10c38c18c19b5"></a>

### JSON<a name="aws-properties-as-launchconfig-blockdev-mapping-syntax.json"></a>

```
{
   "[DeviceName](#cfn-as-launchconfig-blockdev-mapping-devicename)" : String,
   "[Ebs](#cfn-as-launchconfig-blockdev-mapping-ebs)" : AutoScaling EBS Block Device,
   "[NoDevice](#cfn-as-launchconfig-blockdev-mapping-nodevice)" : Boolean,
   "[VirtualName](#cfn-as-launchconfig-blockdev-mapping-virtualname)" : String
}
```

### YAML<a name="aws-properties-as-launchconfig-blockdev-mapping-syntax.yaml"></a>

```
[DeviceName](#cfn-as-launchconfig-blockdev-mapping-devicename): String
[Ebs](#cfn-as-launchconfig-blockdev-mapping-ebs):
  AutoScaling EBS Block Device
[NoDevice](#cfn-as-launchconfig-blockdev-mapping-nodevice): Boolean
[VirtualName](#cfn-as-launchconfig-blockdev-mapping-virtualname): String
```

## Properties<a name="w2922ab1c21c10c38c18c19b7"></a>

**Note**  
 For more information about the constraints and valid values of each property, see [Ebs](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_Ebs.html) in the *Amazon EC2 Auto Scaling API Reference*\. 

`DeviceName`  <a name="cfn-as-launchconfig-blockdev-mapping-devicename"></a>
The name of the device within Amazon EC2\.  
*Required*: Yes  
*Type*: String

`Ebs`  <a name="cfn-as-launchconfig-blockdev-mapping-ebs"></a>
The Amazon Elastic Block Store volume information\.  
*Required*: Conditional You can specify either `VirtualName` or `Ebs`, but not both\.  
*Type*: [Amazon EC2 Auto Scaling LaunchConfig BlockDevice](aws-properties-as-launchconfig-blockdev-template.md)\.

`NoDevice`  <a name="cfn-as-launchconfig-blockdev-mapping-nodevice"></a>
Suppresses the device mapping\. If `NoDevice` is set to true for the root device, the instance might fail the Amazon EC2 health check\. Amazon EC2 Auto Scaling launches a replacement instance if the instance fails the health check\.  
*Required*: No  
*Type*: Boolean

`VirtualName`  <a name="cfn-as-launchconfig-blockdev-mapping-virtualname"></a>
The name of the virtual device\. The name must be in the form `ephemeralX ` where *X* is a number starting from zero \(0\), for example, `ephemeral0`\.  
*Required*: Conditional You can specify either `VirtualName` or `Ebs`, but not both\.  
*Type*: String