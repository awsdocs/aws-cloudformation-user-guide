# AWS::ImageBuilder::ImageRecipe EbsInstanceBlockDeviceSpecification<a name="aws-properties-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification"></a>

The image recipe EBS instance block device specification includes the Amazon EBS\-specific block device mapping specifications for the image\.

## Syntax<a name="aws-properties-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-syntax.json"></a>

```
{
  "[DeleteOnTermination](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-deleteontermination)" : Boolean,
  "[Encrypted](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-encrypted)" : Boolean,
  "[Iops](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-iops)" : Integer,
  "[KmsKeyId](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-kmskeyid)" : String,
  "[SnapshotId](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-snapshotid)" : String,
  "[VolumeSize](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-volumesize)" : Integer,
  "[VolumeType](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-volumetype)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-syntax.yaml"></a>

```
  [DeleteOnTermination](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-deleteontermination): Boolean
  [Encrypted](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-encrypted): Boolean
  [Iops](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-iops): Integer
  [KmsKeyId](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-kmskeyid): String
  [SnapshotId](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-snapshotid): String
  [VolumeSize](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-volumesize): Integer
  [VolumeType](#cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-volumetype): String
```

## Properties<a name="aws-properties-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-properties"></a>

`DeleteOnTermination`  <a name="cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-deleteontermination"></a>
Configures delete on termination of the associated device\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Encrypted`  <a name="cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-encrypted"></a>
Use to configure device encryption\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Iops`  <a name="cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-iops"></a>
Use to configure device IOPS\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `100`  
*Maximum*: `10000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-kmskeyid"></a>
Use to configure the KMS key to use when encrypting the device\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotId`  <a name="cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-snapshotid"></a>
The snapshot that defines the device contents\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeSize`  <a name="cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-volumesize"></a>
Overrides the volume size of the device\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `16000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeType`  <a name="cfn-imagebuilder-imagerecipe-ebsinstanceblockdevicespecification-volumetype"></a>
Overrides the volume type of the device\.  
*Required*: No  
*Type*: String  
*Allowed values*: `gp2 | io1 | io2 | sc1 | st1 | standard`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)