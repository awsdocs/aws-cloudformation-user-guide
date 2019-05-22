# AWS::EC2::Volume<a name="aws-properties-ec2-ebs-volume"></a>

Specifies an Amazon Elastic Block Store \(Amazon EBS\) volume\.

When you use AWS CloudFormation to update an Amazon EBS volume that modifies `Iops`, `Size`, or `VolumeType`, there is a cooldown period before another operation can occur\. This can cause your stack to report being in `UPDATE_IN_PROGRESS` or `UPDATE_ROLLBACK_IN_PROGRESS` for long periods of time\.

Amazon EBS does not support modifying a Magnetic volume\. For more information, see [Requirements for Modifying EBS Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/modify-volume-requirements.html)\.

Amazon EBS does not support sizing down an Amazon EBS volume\. AWS CloudFormation will not attempt to modify an Amazon EBS volume to a smaller size on rollback\.

Some common scenarios when you might encounter a cooldown period for Amazon EBS include:
+ You successfully update an Amazon EBS volume and the update succeeds\. When you attempt another update within the cooldown window, that update will be subject to a cooldown period\.
+ You successfully update an Amazon EBS volume and the update succeeds but another change in your `update-stack` call fails\. The rollback will be subject to a cooldown period\.

For more information on the cooldown period, see [Requirements for Modifying EBS Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/modify-volume-requirements.html)\.

To control how AWS CloudFormation handles the volume when the stack is deleted, set a deletion policy for your volume\. You can choose to retain the volume, to delete the volume, or to create a snapshot of the volume\. For more information, see [DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

**Note**  
If you set a deletion policy that creates a snapshot, all tags on the volume are included in the snapshot\.

## Syntax<a name="aws-properties-ec2-ebs-volume-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ebs-volume-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Volume",
  "Properties" : {
      "[AutoEnableIO](#cfn-ec2-ebs-volume-autoenableio)" : Boolean,
      "[AvailabilityZone](#cfn-ec2-ebs-volume-availabilityzone)" : String,
      "[Encrypted](#cfn-ec2-ebs-volume-encrypted)" : Boolean,
      "[Iops](#cfn-ec2-ebs-volume-iops)" : Integer,
      "[KmsKeyId](#cfn-ec2-ebs-volume-kmskeyid)" : String,
      "[Size](#cfn-ec2-ebs-volume-size)" : Integer,
      "[SnapshotId](#cfn-ec2-ebs-volume-snapshotid)" : String,
      "[Tags](#cfn-ec2-ebs-volume-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VolumeType](#cfn-ec2-ebs-volume-volumetype)" : String
    }
}
```

### YAML<a name="aws-properties-ec2-ebs-volume-syntax.yaml"></a>

```
Type: AWS::EC2::Volume
Properties: 
  [AutoEnableIO](#cfn-ec2-ebs-volume-autoenableio): Boolean
  [AvailabilityZone](#cfn-ec2-ebs-volume-availabilityzone): String
  [Encrypted](#cfn-ec2-ebs-volume-encrypted): Boolean
  [Iops](#cfn-ec2-ebs-volume-iops): Integer
  [KmsKeyId](#cfn-ec2-ebs-volume-kmskeyid): String
  [Size](#cfn-ec2-ebs-volume-size): Integer
  [SnapshotId](#cfn-ec2-ebs-volume-snapshotid): String
  [Tags](#cfn-ec2-ebs-volume-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VolumeType](#cfn-ec2-ebs-volume-volumetype): String
```

## Properties<a name="aws-properties-ec2-ebs-volume-properties"></a>

`AutoEnableIO`  <a name="cfn-ec2-ebs-volume-autoenableio"></a>
Indicates whether the volume is auto\-enabled for I/O operations\. By default, Amazon EBS disables I/O to the volume from attached EC2 instances when it determines that a volume's data is potentially inconsistent\. If the consistency of the volume is not a concern, and you prefer that the volume be made available immediately if it's impaired, you can configure the volume to automatically enable I/O\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-ebs-volume-availabilityzone"></a>
The Availability Zone in which to create the new volume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encrypted`  <a name="cfn-ec2-ebs-volume-encrypted"></a>
Indicates whether the volume is encrypted\. You can attach encrypted Amazon EBS volumes only to instance types that support Amazon EBS encryption\. Volumes that are created from encrypted snapshots are automatically encrypted\. You can't create an encrypted volume from an unencrypted snapshot, or vice versa\. If your AMI uses encrypted volumes, you can launch the AMI only on supported instance types\.  
Requirement is conditional: If you specify the `KmsKeyId` property, you must enable encryption\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Iops`  <a name="cfn-ec2-ebs-volume-iops"></a>
The number of I/O operations per second \(IOPS\) that the volume supports\. For Provisioned IOPS SSD volumes, this represents the number of IOPS that are provisioned for the volume\. For General Purpose SSD volumes, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\. For more information, see [Amazon EBS Volume Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Constraints: Range is 100\-16,000 IOPS for `gp2` volumes and 100 to 64,000IOPS for `io1` volumes, in most Regions\. The maximum IOPS for `io1` of 64,000 is guaranteed only on [Nitro\-based instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\.  
Requirement is conditional: This parameter is required for requests to create `io1` volumes; it is not used in requests to create `gp2`, `st1`, `sc1`, or `standard` volumes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-ec2-ebs-volume-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service master key that is used to create the encrypted volume, such as `arn:aws:kms:us-east-2:012345678910:key/abcd1234-a123-456a-a12b-a123b4cd56ef`\. If you create an encrypted volume and don't specify this property, AWS CloudFormation uses the default master key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-ec2-ebs-volume-size"></a>
The size of the volume, in gibibytes \(GiBs\)\.  
 If you specify the `SnapshotId` property, specify a size that is equal to or greater than the size of the snapshot\. If you don't specify a size, EC2 uses the size of the snapshot as the volume size\.  
Requirement is conditional: If you don't specify a value for the `SnapshotId` property, then you must specify this property\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-ec2-ebs-volume-snapshotid"></a>
The snapshot from which to create the volume\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-ebs-volume-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this volume\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-ebs-volume-volumetype"></a>
The volume type\. This can be `gp2` for General Purpose SSD, `io1` for Provisioned IOPS SSD, `st1` for Throughput Optimized HDD, `sc1` for Cold HDD, or `standard` for Magnetic volumes\. If you set the type to `io1`, you must also set the `Iops` property\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `gp2 | io1 | sc1 | st1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-properties-ec2-ebs-volume-return-values"></a>

### Ref<a name="aws-properties-ec2-ebs-volume-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example: `vol-5cb85026`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-ec2-ebs-volume--examples"></a>

### Encrypted Amazon EBS Volume with DeletionPolicy to Make a Snapshot on Delete<a name="aws-properties-ec2-ebs-volume--examples--Encrypted_Amazon_EBS_Volume_with_DeletionPolicy_to_Make_a_Snapshot_on_Delete"></a>

#### JSON<a name="aws-properties-ec2-ebs-volume--examples--Encrypted_Amazon_EBS_Volume_with_DeletionPolicy_to_Make_a_Snapshot_on_Delete--json"></a>

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

#### YAML<a name="aws-properties-ec2-ebs-volume--examples--Encrypted_Amazon_EBS_Volume_with_DeletionPolicy_to_Make_a_Snapshot_on_Delete--yaml"></a>

```
NewVolume:
  Type: AWS::EC2::Volume
  Properties:
    Size: 100
    Encrypted: true
    AvailabilityZone: !GetAtt Ec2Instance.AvailabilityZone
    Tags:
      - Key: MyTag
        Value: TagValue
  DeletionPolicy: Snapshot
```

### Amazon EBS Volume with 100 Provisioned IOPS<a name="aws-properties-ec2-ebs-volume--examples--Amazon_EBS_Volume_with_100_Provisioned_IOPS"></a>

#### JSON<a name="aws-properties-ec2-ebs-volume--examples--Amazon_EBS_Volume_with_100_Provisioned_IOPS--json"></a>

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

#### YAML<a name="aws-properties-ec2-ebs-volume--examples--Amazon_EBS_Volume_with_100_Provisioned_IOPS--yaml"></a>

```
NewVolume:
  Type: AWS::EC2::Volume
  Properties:
    Size: 100
    VolumeType: io1
    Iops: 100
    AvailabilityZone: !GetAtt Ec2Instance.AvailabilityZone
```

## See Also<a name="aws-properties-ec2-ebs-volume--seealso"></a>
+  [ CreateVolume](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVolume.html) in the *Amazon Elastic Compute Cloud API Reference*
