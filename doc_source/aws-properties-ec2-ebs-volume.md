# AWS::EC2::Volume<a name="aws-properties-ec2-ebs-volume"></a>

The `AWS::EC2::Volume` type creates a new Amazon Elastic Block Store \(Amazon EBS\) volume\.

**Important**  
When you use AWS CloudFormation to update an Amazon EBS volume that modifies `Iops`, `Size`, or `VolumeType`, there is a cooldown period before another operation can occur\. This can cause your stack to report being in `UPDATE_IN_PROGRESS` or `UPDATE_ROLLBACK_IN_PROGRESS` for long periods of time\.

Some common scenarios when you might encounter a cooldown period for Amazon EBS include:
+ You successfully update an Amazon EBS volume and the update succeeds\. When you attempt another update within the cooldown window, that update will be subject to a cooldown period\.
+ You successfully update an Amazon EBS volume and the update succeeds but another change in your `update-stack` call fails\. The rollback will be subject to a cooldown period\.

For more information on the cooldown period, see [Considerations for Modifying EBS Volumes](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/considerations.html) in the *Amazon EBS Developer Guide*\.

To control how AWS CloudFormation handles the volume when the stack is deleted, set a deletion policy for your volume\. You can choose to *retain* the volume, to *delete* the volume, or to *create a snapshot* of the volume\. For more information, see [DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)\.

**Note**  
If you set a deletion policy that creates a snapshot, all tags on the volume are included in the snapshot\.

**Important**  
Amazon EBS does not support sizing down an Amazon EBS volume\. AWS CloudFormation will not attempt to modify an Amazon EBS volume to a smaller size on rollback\.

**Note**  
Amazon EBS does not support modifying a Magnetic volume\. For more information, see [Considerations for Modifying EBS Volumes](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/considerations.html)\.

**Topics**
+ [Syntax](#aws-resource-ec2-volume-syntax)
+ [Properties](#w3ab2c21c10d502c25)
+ [Return Values](#w3ab2c21c10d502c27)
+ [Examples](#w3ab2c21c10d502c29)
+ [More Info](#w3ab2c21c10d502c31)

## Syntax<a name="aws-resource-ec2-volume-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-volume-syntax.json"></a>

```
{
   "Type":"AWS::EC2::Volume",
   "Properties" : {
      "[AutoEnableIO](#cfn-ec2-ebs-volume-autoenableio)" : Boolean,
      "[AvailabilityZone](#cfn-ec2-ebs-volume-availabilityzone)" : String,
      "[Encrypted](#cfn-ec2-ebs-volume-encrypted)" : Boolean,
      "[Iops](#cfn-ec2-ebs-volume-iops)" : Number,
      "[KmsKeyId](#cfn-ec2-ebs-volume-kmskeyid)" : String,
      "[Size](#cfn-ec2-ebs-volume-size)" : Integer,
      "[SnapshotId](#cfn-ec2-ebs-volume-snapshotid)" : String,
      "[Tags](#cfn-ec2-ebs-volume-tags)" : [ Resource Tag, ... ],
      "[VolumeType](#cfn-ec2-ebs-volume-volumetype)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-volume-syntax.yaml"></a>

```
Type: "AWS::EC2::Volume"
Properties:
  [AutoEnableIO](#cfn-ec2-ebs-volume-autoenableio): Boolean
  [AvailabilityZone](#cfn-ec2-ebs-volume-availabilityzone): String
  [Encrypted](#cfn-ec2-ebs-volume-encrypted): Boolean
  [Iops](#cfn-ec2-ebs-volume-iops): Number
  [KmsKeyId](#cfn-ec2-ebs-volume-kmskeyid): String
  [Size](#cfn-ec2-ebs-volume-size): Integer
  [SnapshotId](#cfn-ec2-ebs-volume-snapshotid): String
  [Tags](#cfn-ec2-ebs-volume-tags):
    - Resource Tag
  [VolumeType](#cfn-ec2-ebs-volume-volumetype): String
```

## Properties<a name="w3ab2c21c10d502c25"></a>

`AutoEnableIO`  <a name="cfn-ec2-ebs-volume-autoenableio"></a>
Indicates whether the volume is auto\-enabled for I/O operations\. By default, Amazon EBS disables I/O to the volume from attached EC2 instances when it determines that a volume's data is potentially inconsistent\. If the consistency of the volume is not a concern, and you prefer that the volume be made available immediately if it's impaired, you can configure the volume to automatically enable I/O\. For more information, see [Working with the AutoEnableIO Volume Attribute](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/monitoring-volume-status.html#volumeIO) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-ebs-volume-availabilityzone"></a>
The Availability Zone in which to create the new volume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Encrypted`  <a name="cfn-ec2-ebs-volume-encrypted"></a>
Indicates whether the volume is encrypted\. You can attach encrypted Amazon EBS volumes only to instance types that support Amazon EBS encryption\. Volumes that are created from encrypted snapshots are automatically encrypted\. You can't create an encrypted volume from an unencrypted snapshot, or vice versa\. If your AMI uses encrypted volumes, you can launch the AMI only on supported instance types\. For more information, see [Amazon EBS encryption](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: Conditional\. If you specify the `KmsKeyId` property, you must enable encryption\.  
*Type*: Boolean  
*Update requires*: Updates are not supported\.

`Iops`  <a name="cfn-ec2-ebs-volume-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. For more information about the valid sizes for each volume type, see the `Iops` parameter for the [http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) action in the *Amazon EC2 API Reference*\.  
*Required*: Conditional\. *Required* when the volume type is `io1`; not used with other volume types\.  
*Type*: Number  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KmsKeyId`  <a name="cfn-ec2-ebs-volume-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service master key that is used to create the encrypted volume, such as `arn:aws:kms:``us-east-2``:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you create an encrypted volume and don't specify this property, AWS CloudFormation uses the default master key\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Size`  <a name="cfn-ec2-ebs-volume-size"></a>
The size of the volume, in gibibytes \(GiBs\)\. For more information about the valid sizes for each volume type, see the `Size` parameter for the [http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) action in the *Amazon EC2 API Reference*\.  
If you specify the `SnapshotId` property, specify a size that is equal to or greater than the size of the snapshot\. If you don't specify a size, EC2 uses the size of the snapshot as the volume size\.  
*Required*: Conditional\. If you don't specify a value for the `SnapshotId` property, you must specify this property\.  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SnapshotId`  <a name="cfn-ec2-ebs-volume-snapshotid"></a>
The snapshot from which to create the new volume\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Tags`  <a name="cfn-ec2-ebs-volume-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this volume\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-ebs-volume-volumetype"></a>
The volume type\. If you set the type to `io1`, you must also set the `Iops` property\. For valid values, see the `VolumeType` parameter for the [CreateVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) action in the *Amazon EC2 API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d502c27"></a>

### Ref<a name="w3ab2c21c10d502c27b2"></a>

When you specify an `AWS::EC2::Volume` type as an argument to the `Ref` function, AWS CloudFormation returns the volume's physical ID\. For example: `vol-5cb85026`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d502c29"></a>

**Example Encrypted Amazon EBS Volume with DeletionPolicy to Make a Snapshot on Delete**  

```
"NewVolume" : {
   "Type" : "AWS::EC2::Volume",
   "Properties" : {
      "Size" : "100",
      "Encrypted" : "true",
      "AvailabilityZone" : { "Fn::GetAtt" : [ "Ec2Instance", "AvailabilityZone" ] },
      "Tags" : [ {
         "Key" : "MyTag",
         "Value" : "TagValue"
      } ]
   },
   "DeletionPolicy" : "Snapshot"
}
```

**Example Amazon EBS Volume with 100 Provisioned IOPS**  

```
"NewVolume" : {
   "Type" : "AWS::EC2::Volume",
   "Properties" : {
     "Size" : "100",
     "VolumeType" : "io1",
     "Iops" : "100",
     "AvailabilityZone" : { "Fn::GetAtt" : [ "EC2Instance", "AvailabilityZone" ] }
   }
}
```

## More Info<a name="w3ab2c21c10d502c31"></a>
+ [CreateVolume](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVolume.html) in the *Amazon Elastic Compute Cloud API Reference*
+ [DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)