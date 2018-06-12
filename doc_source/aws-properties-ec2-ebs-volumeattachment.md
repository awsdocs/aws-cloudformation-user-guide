# AWS::EC2::VolumeAttachment<a name="aws-properties-ec2-ebs-volumeattachment"></a>

Attaches an Amazon EBS volume to a running instance and exposes it to the instance with the specified device name\.

**Important**  
Before this resource can be deleted \(and therefore the volume detached\), you must first unmount the volume in the instance\. Failure to do so results in the volume being stuck in the busy state while it is trying to detach, which could possibly damage the file system or the data it contains\.  
If an Amazon EBS volume is the root device of an instance, it cannot be detached while the instance is in the "running" state\. To detach the root volume, stop the instance first\.  
If the root volume is detached from an instance with an AWS Marketplace product code, then the AWS Marketplace product codes from that volume are no longer associated with the instance\.

**Topics**
+ [Syntax](#aws-resource-ec2-volumeattachment-syntax)
+ [Properties](#w3ab2c21c10d506c11)
+ [Example](#w3ab2c21c10d506c13)
+ [See Also](#w3ab2c21c10d506c15)

## Syntax<a name="aws-resource-ec2-volumeattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-volumeattachment-syntax.json"></a>

```
{
   "Type":"AWS::EC2::VolumeAttachment",
   "Properties" : {
      "[Device](#cfn-ec2-ebs-volumeattachment-device)" : String,
      "[InstanceId](#cfn-ec2-ebs-volumeattachment-instanceid)" : String,
      "[VolumeId](#cfn-ec2-ebs-volumeattachment-volumeid)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-volumeattachment-syntax.yaml"></a>

```
Type: AWS::EC2::VolumeAttachment
Properties:
  [Device](#cfn-ec2-ebs-volumeattachment-device): String
  [InstanceId](#cfn-ec2-ebs-volumeattachment-instanceid): String
  [VolumeId](#cfn-ec2-ebs-volumeattachment-volumeid): String
```

## Properties<a name="w3ab2c21c10d506c11"></a>

`Device`  <a name="cfn-ec2-ebs-volumeattachment-device"></a>
How the device is exposed to the instance \(e\.g\., /dev/sdh, or xvdh\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`InstanceId`  <a name="cfn-ec2-ebs-volumeattachment-instanceid"></a>
The ID of the instance to which the volume attaches\. This value can be a reference to an [AWS::EC2::Instance](aws-properties-ec2-instance.md) resource, or it can be the physical ID of an existing EC2 instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`VolumeId`  <a name="cfn-ec2-ebs-volumeattachment-volumeid"></a>
The ID of the Amazon EBS volume\. The volume and instance must be within the same Availability Zone\. This value can be a reference to an [AWS::EC2::Volume](aws-properties-ec2-ebs-volume.md) resource, or it can be the volume ID of an existing Amazon EBS volume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

## Example<a name="w3ab2c21c10d506c13"></a>

This example attaches an EC2 EBS volume to the EC2 instance with the logical name "Ec2Instance"\.

```
"NewVolume" : {
   "Type" : "AWS::EC2::Volume",
   "Properties" : {
      "Size" : "100",
      "AvailabilityZone" : { "Fn::GetAtt" : [ "Ec2Instance", "AvailabilityZone" ] },
      "Tags" : [ {
         "Key" : "MyTag",
         "Value" : "TagValue"
      } ]
   }
},

"MountPoint" : {
   "Type" : "AWS::EC2::VolumeAttachment",
   "Properties" : {
      "InstanceId" : { "Ref" : "Ec2Instance" },
      "VolumeId"  : { "Ref" : "NewVolume" },
      "Device" : "/dev/sdh"
   }
}
```

## See Also<a name="w3ab2c21c10d506c15"></a>
+ [Amazon Elastic Block Store \(Amazon EBS\)](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html) in the *Amazon Elastic Compute Cloud User Guide*\.
+ [Attaching a Volume to an Instance](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-attaching-volume.html) in the *Amazon Elastic Compute Cloud User Guide*
+ [Detaching an Amazon EBS Volume from an Instance](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-detaching-volume.html) in the *Amazon Elastic Compute Cloud User Guide*
+ [AttachVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-AttachVolume.html) in the *Amazon Elastic Compute Cloud API Reference*
+ [DetachVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-DetachVolume.html) in the *Amazon Elastic Compute Cloud API Reference*