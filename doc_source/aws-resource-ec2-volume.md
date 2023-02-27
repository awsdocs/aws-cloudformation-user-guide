# AWS::EC2::Volume<a name="aws-resource-ec2-volume"></a>

Specifies an Amazon Elastic Block Store \(Amazon EBS\) volume\. You can attach the volume to an instance in the same Availability Zone using [AWS::EC2::VolumeAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volumeattachment.html)\.

When you use AWS CloudFormation to update an Amazon EBS volume that modifies `Iops`, `Size`, or `VolumeType`, there is a cooldown period before another operation can occur\. This can cause your stack to report being in `UPDATE_IN_PROGRESS` or `UPDATE_ROLLBACK_IN_PROGRESS` for long periods of time\.

Amazon EBS does not support sizing down an Amazon EBS volume\. AWS CloudFormation does not attempt to modify an Amazon EBS volume to a smaller size on rollback\.

Some common scenarios when you might encounter a cooldown period for Amazon EBS include:
+ You successfully update an Amazon EBS volume and the update succeeds\. When you attempt another update within the cooldown window, that update will be subject to a cooldown period\.
+ You successfully update an Amazon EBS volume and the update succeeds but another change in your `update-stack` call fails\. The rollback will be subject to a cooldown period\.

For more information on the cooldown period, see [Requirements when modifying volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/modify-volume-requirements.html)\.

**DeletionPolicy attribute**

To control how AWS CloudFormation handles the volume when the stack is deleted, set a deletion policy for your volume\. You can choose to retain the volume, to delete the volume, or to create a snapshot of the volume\. For more information, see [DeletionPolicy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

**Note**  
If you set a deletion policy that creates a snapshot, all tags on the volume are included in the snapshot\.

## Syntax<a name="aws-resource-ec2-volume-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-volume-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Volume",
  "Properties" : {
      "[AutoEnableIO](#cfn-ec2-volume-autoenableio)" : Boolean,
      "[AvailabilityZone](#cfn-ec2-volume-availabilityzone)" : String,
      "[Encrypted](#cfn-ec2-volume-encrypted)" : Boolean,
      "[Iops](#cfn-ec2-volume-iops)" : Integer,
      "[KmsKeyId](#cfn-ec2-volume-kmskeyid)" : String,
      "[MultiAttachEnabled](#cfn-ec2-volume-multiattachenabled)" : Boolean,
      "[OutpostArn](#cfn-ec2-volume-outpostarn)" : String,
      "[Size](#cfn-ec2-volume-size)" : Integer,
      "[SnapshotId](#cfn-ec2-volume-snapshotid)" : String,
      "[Tags](#cfn-ec2-volume-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Throughput](#cfn-ec2-volume-throughput)" : Integer,
      "[VolumeType](#cfn-ec2-volume-volumetype)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-volume-syntax.yaml"></a>

```
Type: AWS::EC2::Volume
Properties: 
  [AutoEnableIO](#cfn-ec2-volume-autoenableio): Boolean
  [AvailabilityZone](#cfn-ec2-volume-availabilityzone): String
  [Encrypted](#cfn-ec2-volume-encrypted): Boolean
  [Iops](#cfn-ec2-volume-iops): Integer
  [KmsKeyId](#cfn-ec2-volume-kmskeyid): String
  [MultiAttachEnabled](#cfn-ec2-volume-multiattachenabled): Boolean
  [OutpostArn](#cfn-ec2-volume-outpostarn): String
  [Size](#cfn-ec2-volume-size): Integer
  [SnapshotId](#cfn-ec2-volume-snapshotid): String
  [Tags](#cfn-ec2-volume-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Throughput](#cfn-ec2-volume-throughput): Integer
  [VolumeType](#cfn-ec2-volume-volumetype): String
```

## Properties<a name="aws-resource-ec2-volume-properties"></a>

`AutoEnableIO`  <a name="cfn-ec2-volume-autoenableio"></a>
Indicates whether the volume is auto\-enabled for I/O operations\. By default, Amazon EBS disables I/O to the volume from attached EC2 instances when it determines that a volume's data is potentially inconsistent\. If the consistency of the volume is not a concern, and you prefer that the volume be made available immediately if it's impaired, you can configure the volume to automatically enable I/O\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-volume-availabilityzone"></a>
The Availability Zone in which to create the volume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Encrypted`  <a name="cfn-ec2-volume-encrypted"></a>
Indicates whether the volume should be encrypted\. The effect of setting the encryption state to `true` depends on the volume origin \(new or from a snapshot\), starting encryption state, ownership, and whether encryption by default is enabled\. For more information, see [Encryption by default](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#encryption-by-default) in the *Amazon Elastic Compute Cloud User Guide*\.  
Encrypted Amazon EBS volumes must be attached to instances that support Amazon EBS encryption\. For more information, see [Supported instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html#EBSEncryption_supported_instances)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: Updates are not supported\.

`Iops`  <a name="cfn-ec2-volume-iops"></a>
The number of I/O operations per second \(IOPS\)\. For `gp3`, `io1`, and `io2` volumes, this represents the number of IOPS that are provisioned for the volume\. For `gp2` volumes, this represents the baseline performance of the volume and the rate at which the volume accumulates I/O credits for bursting\.  
The following are the supported values for each volume type:  
+  `gp3`: 3,000\-16,000 IOPS
+  `io1`: 100\-64,000 IOPS
+  `io2`: 100\-64,000 IOPS
 `io1` and `io2` volumes support up to 64,000 IOPS only on [Instances built on the Nitro System](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances)\. Other instance families support performance up to 32,000 IOPS\.  
This parameter is required for `io1` and `io2` volumes\. The default for `gp3` volumes is 3,000 IOPS\. This parameter is not supported for `gp2`, `st1`, `sc1`, or `standard` volumes\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-ec2-volume-kmskeyid"></a>
The identifier of the AWS KMS key to use for Amazon EBS encryption\. If `KmsKeyId` is specified, the encrypted state must be `true`\.  
If you omit this property and your account is enabled for encryption by default, or **Encrypted** is set to `true`, then the volume is encrypted using the default key specified for your account\. If your account does not have a default key, then the volume is encrypted using the AWS managed key\.  
Alternatively, if you want to specify a different key, you can specify one of the following:  
+ Key ID\. For example, 1234abcd\-12ab\-34cd\-56ef\-1234567890ab\.
+ Key alias\. Specify the alias for the key, prefixed with `alias/`\. For example, for a key with the alias `my_cmk`, use `alias/my_cmk`\. Or to specify the AWS managed key, use `alias/aws/ebs`\.
+ Key ARN\. For example, arn:aws:kms:us\-east\-1:012345678910:key/1234abcd\-12ab\-34cd\-56ef\-1234567890ab\.
+ Alias ARN\. For example, arn:aws:kms:us\-east\-1:012345678910:alias/ExampleAlias\.
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`MultiAttachEnabled`  <a name="cfn-ec2-volume-multiattachenabled"></a>
Indicates whether Amazon EBS Multi\-Attach is enabled\.  
AWS CloudFormation does not currently support updating a single\-attach volume to be multi\-attach enabled, updating a multi\-attach enabled volume to be single\-attach, or updating the size or number of I/O operations per second \(IOPS\) of a multi\-attach enabled volume\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutpostArn`  <a name="cfn-ec2-volume-outpostarn"></a>
The Amazon Resource Name \(ARN\) of the Outpost\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-ec2-volume-size"></a>
The size of the volume, in GiBs\. You must specify either a snapshot ID or a volume size\. If you specify a snapshot, the default is the snapshot size\. You can specify a volume size that is equal to or larger than the snapshot size\.  
The following are the supported volumes sizes for each volume type:  
+  `gp2` and `gp3`: 1\-16,384
+  `io1` and `io2`: 4\-16,384
+  `st1` and `sc1`: 125\-16,384
+  `standard`: 1\-1,024
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotId`  <a name="cfn-ec2-volume-snapshotid"></a>
The snapshot from which to create the volume\. You must specify either a snapshot ID or a volume size\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: Updates are not supported\.

`Tags`  <a name="cfn-ec2-volume-tags"></a>
The tags to apply to the volume during creation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Throughput`  <a name="cfn-ec2-volume-throughput"></a>
The throughput to provision for a volume, with a maximum of 1,000 MiB/s\.  
This parameter is valid only for `gp3` volumes\. The default value is 125\.  
Valid Range: Minimum value of 125\. Maximum value of 1000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeType`  <a name="cfn-ec2-volume-volumetype"></a>
The volume type\. This parameter can be one of the following values:  
+ General Purpose SSD: `gp2` \| `gp3` 
+ Provisioned IOPS SSD: `io1` \| `io2` 
+ Throughput Optimized HDD: `st1` 
+ Cold HDD: `sc1` 
+ Magnetic: `standard` 
For more information, see [Amazon EBS volume types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
Default: `gp2`   
*Required*: No  
*Type*: String  
*Allowed values*: `gp2 | gp3 | io1 | io2 | sc1 | st1 | standard`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-volume-return-values"></a>

### Ref<a name="aws-resource-ec2-volume-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example: `vol-5cb85026`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-volume-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-volume-return-values-fn--getatt-fn--getatt"></a>

`VolumeId`  <a name="VolumeId-fn::getatt"></a>
The ID of the volume\.

## Examples<a name="aws-resource-ec2-volume--examples"></a>



### Encrypted Amazon EBS volume with DeletionPolicy<a name="aws-resource-ec2-volume--examples--Encrypted_Amazon_EBS_volume_with_DeletionPolicy"></a>

The following example creates an encrypted `gp2` volume with a DeletionPolicy attribute that creates a snapshot of the volume when the stack is deleted\.

#### JSON<a name="aws-resource-ec2-volume--examples--Encrypted_Amazon_EBS_volume_with_DeletionPolicy--json"></a>

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

#### YAML<a name="aws-resource-ec2-volume--examples--Encrypted_Amazon_EBS_volume_with_DeletionPolicy--yaml"></a>

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

### Provisioned IOPS SSD io1 volume<a name="aws-resource-ec2-volume--examples--Provisioned_IOPS_SSD_io1_volume"></a>

The following example creates a 100 GiB `io1` with `100` provisioned IOPS\.

#### JSON<a name="aws-resource-ec2-volume--examples--Provisioned_IOPS_SSD_io1_volume--json"></a>

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

#### YAML<a name="aws-resource-ec2-volume--examples--Provisioned_IOPS_SSD_io1_volume--yaml"></a>

```
NewVolume:
  Type: AWS::EC2::Volume
  Properties: 
    Size: 100
    VolumeType: io1
    Iops: 100
    AvailabilityZone: !GetAtt Ec2Instance.AvailabilityZone
```

## See also<a name="aws-resource-ec2-volume--seealso"></a>
+  [ CreateVolume](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVolume.html) in the *Amazon EC2 API Reference*