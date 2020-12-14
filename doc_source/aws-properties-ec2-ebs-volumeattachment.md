# AWS::EC2::VolumeAttachment<a name="aws-properties-ec2-ebs-volumeattachment"></a>

Attaches an Amazon EBS volume to a running instance and exposes it to the instance with the specified device name\.

Before this resource can be deleted \(and therefore the volume detached\), you must first unmount the volume in the instance\. Failure to do so results in the volume being stuck in the busy state while it is trying to detach, which could possibly damage the file system or the data it contains\.

If an Amazon EBS volume is the root device of an instance, it cannot be detached while the instance is in the "running" state\. To detach the root volume, stop the instance first\.

If the root volume is detached from an instance with an AWS Marketplace product code, then the AWS Marketplace product codes from that volume are no longer associated with the instance\.

## Syntax<a name="aws-properties-ec2-ebs-volumeattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ebs-volumeattachment-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VolumeAttachment",
  "Properties" : {
      "[Device](#cfn-ec2-ebs-volumeattachment-device)" : String,
      "[InstanceId](#cfn-ec2-ebs-volumeattachment-instanceid)" : String,
      "[VolumeId](#cfn-ec2-ebs-volumeattachment-volumeid)" : String
    }
}
```

### YAML<a name="aws-properties-ec2-ebs-volumeattachment-syntax.yaml"></a>

```
Type: AWS::EC2::VolumeAttachment
Properties: 
  [Device](#cfn-ec2-ebs-volumeattachment-device): String
  [InstanceId](#cfn-ec2-ebs-volumeattachment-instanceid): String
  [VolumeId](#cfn-ec2-ebs-volumeattachment-volumeid): String
```

## Properties<a name="aws-properties-ec2-ebs-volumeattachment-properties"></a>

`Device`  <a name="cfn-ec2-ebs-volumeattachment-device"></a>
The device name \(for example, `/dev/sdh` or `xvdh`\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceId`  <a name="cfn-ec2-ebs-volumeattachment-instanceid"></a>
The ID of the instance to which the volume attaches\. This value can be a reference to an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource, or it can be the physical ID of an existing EC2 instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeId`  <a name="cfn-ec2-ebs-volumeattachment-volumeid"></a>
The ID of the Amazon EBS volume\. The volume and instance must be within the same Availability Zone\. This value can be a reference to an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html) resource, or it can be the volume ID of an existing Amazon EBS volume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-properties-ec2-ebs-volumeattachment--examples"></a>



### Attach an EBS Volume to a Running Instance<a name="aws-properties-ec2-ebs-volumeattachment--examples--Attach_an_EBS_Volume_to_a_Running_Instance"></a>

This example attaches an EC2 EBS volume to the EC2 instance with the logical name "Ec2Instance"\.

#### JSON<a name="aws-properties-ec2-ebs-volumeattachment--examples--Attach_an_EBS_Volume_to_a_Running_Instance--json"></a>

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

#### YAML<a name="aws-properties-ec2-ebs-volumeattachment--examples--Attach_an_EBS_Volume_to_a_Running_Instance--yaml"></a>

```
NewVolume:
  Type: AWS::EC2::Volume
  Properties:
    Size: 100
    AvailabilityZone: !GetAtt Ec2Instance.AvailabilityZone
    Tags:
      - Key: MyTag
        Value: TagValue
  DeletionPolicy: Snapshot

MountPoint:
  Type: AWS::EC2::VolumeAttachment
  Properties:
    InstanceId: !Ref Ec2Instance
    VolumeId: !Ref NewVolume
    Device: /dev/sdh
```

## See also<a name="aws-properties-ec2-ebs-volumeattachment--seealso"></a>
+  [Amazon Elastic Block Store \(Amazon EBS\)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html) in the *Amazon Elastic Compute Cloud User Guide*
+  [Attaching a Volume to an Instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-attaching-volume.html) in the *Amazon Elastic Compute Cloud User Guide* 
+  [Detaching an Amazon EBS Volume from an Instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-detaching-volume.html) in the *Amazon Elastic Compute Cloud User Guide* 
+  [AttachVolume](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-AttachVolume.html) in the *Amazon Elastic Compute Cloud API Reference* 
+  [DetachVolume](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-DetachVolume.html) in the *Amazon Elastic Compute Cloud API Reference* 