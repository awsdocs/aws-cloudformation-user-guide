# AWS::EC2::Instance Volume<a name="aws-properties-ec2-mount-point"></a>

Specifies a volume to attach to an instance\.

 `Volume` is an embedded property of the [ AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

## Syntax<a name="aws-properties-ec2-mount-point-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-mount-point-syntax.json"></a>

```
{
  "[Device](#cfn-ec2-mountpoint-device)" : String,
  "[VolumeId](#cfn-ec2-mountpoint-volumeid)" : String
}
```

### YAML<a name="aws-properties-ec2-mount-point-syntax.yaml"></a>

```
  [Device](#cfn-ec2-mountpoint-device): String
  [VolumeId](#cfn-ec2-mountpoint-volumeid): String
```

## Properties<a name="aws-properties-ec2-mount-point-properties"></a>

`Device`  <a name="cfn-ec2-mountpoint-device"></a>
The device name \(for example, `/dev/sdh` or `xvdh`\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeId`  <a name="cfn-ec2-mountpoint-volumeid"></a>
The ID of the EBS volume\. The volume and instance must be within the same Availability Zone\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)