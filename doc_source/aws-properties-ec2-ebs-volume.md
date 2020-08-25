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
      "[MultiAttachEnabled](#cfn-ec2-ebs-volume-multiattachenabled)" : Boolean,
      "[OutpostArn](#cfn-ec2-ebs-volume-outpostarn)" : String,
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
  [MultiAttachEnabled](#cfn-ec2-ebs-volume-multiattachenabled): Boolean
  [OutpostArn](#cfn-ec2-ebs-volume-outpostarn): String
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
The Availability Zone in which to create the volume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Encrypted`  <a name="cfn-ec2-ebs-volume-encrypted"></a>
Specifies whether the volume should be encrypted\. The effect of setting the encryption state to `true` depends on the volume origin \(new or from a snapshot\), starting encryption state, ownership, and whether encryption by default is enabled\. For more information, see [Encryption by default](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#encryption-by-default) in the *Amazon Elastic Compute Cloud User Guide*\.  
Encrypted Amazon EBS volumes must be attached to instances that support Amazon EBS encryption\. For more information, see [Supported instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#EBSEncryption_supported_instances)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: Updates are not supported\.

`Iops`  <a name="cfn-ec2-ebs-volume-iops"></a>
The number of I/O operations per second \(IOPS\) to provision for an `io1` or `io2` volume, with a maximum ratio of 50 IOPS/GiB for `io1`, and 500 IOPS/GiB for `io2`\. Range is 100 to 64,000 IOPS for volumes in most Regions\. Maximum IOPS of 64,000 is guaranteed only on [Nitro\-based instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families guarantee performance up to 32,000 IOPS\. For more information, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
This parameter is valid only for Provisioned IOPS SSD \(`io1` and `io2`\) volumes\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-ec2-ebs-volume-kmskeyid"></a>
The identifier of the AWS Key Management Service \(AWS KMS\) customer master key \(CMK\) to use for Amazon EBS encryption\. If this parameter is not specified, your AWS managed CMK for EBS is used\. If `KmsKeyId` is specified, the encrypted state must be `true`\.  
You can specify the CMK using any of the following:  
+ Key ID\. For example, key/1234abcd\-12ab\-34cd\-56ef\-1234567890ab\.
+ Key alias\. For example, alias/ExampleAlias\.
+ Key ARN\. For example, arn:aws:kms:*us\-east\-1*:*012345678910*:key/*abcd1234\-a123\-456a\-a12b\-a123b4cd56ef*\.
+ Alias ARN\. For example, arn:aws:kms:*us\-east\-1*:*012345678910*:alias/*ExampleAlias*\.
AWS authenticates the CMK asynchronously\. Therefore, if you specify an ID, alias, or ARN that is not valid, the action can appear to complete, but eventually fails\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`MultiAttachEnabled`  <a name="cfn-ec2-ebs-volume-multiattachenabled"></a>
Indicates whether Amazon EBS Multi\-Attach is enabled\.  
AWS CloudFormation does not currently support updating a single\-attach volume to be multi\-attach enabled, updating a multi\-attach enabled volume to be single\-attach, or updating the size or number of I/O operations per second \(IOPS\) of a multi\-attach enabled volume\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutpostArn`  <a name="cfn-ec2-ebs-volume-outpostarn"></a>
The Amazon Resource Name \(ARN\) of the Outpost\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-ec2-ebs-volume-size"></a>
The size of the volume, in GiBs\. You must specify either a snapshot ID or a volume size\.  
Constraints: 1\-16,384 for `gp2`, 4\-16,384 for `io1` and `io2`, 500\-16,384 for `st1`, 500\-16,384 for `sc1`, and 1\-1,024 for `standard`\. If you specify a snapshot, the volume size must be equal to or larger than the snapshot size\.  
Default: If you're creating the volume from a snapshot and don't specify a volume size, the default is the snapshot size\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-ec2-ebs-volume-snapshotid"></a>
The snapshot from which to create the volume\. You must specify either a snapshot ID or a volume size\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Tags`  <a name="cfn-ec2-ebs-volume-tags"></a>
The tags to apply to the volume during creation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-ebs-volume-volumetype"></a>
The volume type\. This can be `gp2` for General Purpose SSD, `io1` or `io2` for Provisioned IOPS SSD, `st1` for Throughput Optimized HDD, `sc1` for Cold HDD, or `standard` for Magnetic volumes\.  
Default: `gp2`   
*Required*: No  
*Type*: String  
*Allowed values*: `gp2 | io1 | io2 | sc1 | st1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-ec2-ebs-volume-return-values"></a>

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

## See also<a name="aws-properties-ec2-ebs-volume--seealso"></a>
+  [ CreateVolume](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVolume.html) in the *Amazon Elastic Compute Cloud API Reference*