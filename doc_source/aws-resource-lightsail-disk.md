# AWS::Lightsail::Disk<a name="aws-resource-lightsail-disk"></a>

The `AWS::Lightsail::Disk` resource specifies a disk that can be attached to an Amazon Lightsail instance that is in the same AWS Region and Availability Zone\.

## Syntax<a name="aws-resource-lightsail-disk-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lightsail-disk-syntax.json"></a>

```
{
  "Type" : "AWS::Lightsail::Disk",
  "Properties" : {
      "[AddOns](#cfn-lightsail-disk-addons)" : [ AddOn, ... ],
      "[AvailabilityZone](#cfn-lightsail-disk-availabilityzone)" : String,
      "[DiskName](#cfn-lightsail-disk-diskname)" : String,
      "[SizeInGb](#cfn-lightsail-disk-sizeingb)" : Integer,
      "[Tags](#cfn-lightsail-disk-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-lightsail-disk-syntax.yaml"></a>

```
Type: AWS::Lightsail::Disk
Properties: 
  [AddOns](#cfn-lightsail-disk-addons): 
    - AddOn
  [AvailabilityZone](#cfn-lightsail-disk-availabilityzone): String
  [DiskName](#cfn-lightsail-disk-diskname): String
  [SizeInGb](#cfn-lightsail-disk-sizeingb): Integer
  [Tags](#cfn-lightsail-disk-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-lightsail-disk-properties"></a>

`AddOns`  <a name="cfn-lightsail-disk-addons"></a>
An array of add\-ons for the disk\.  
If the disk has an add\-on enabled when performing a delete disk request, the add\-on is automatically disabled before the disk is deleted\.
*Required*: No  
*Type*: List of [AddOn](aws-properties-lightsail-disk-addon.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-lightsail-disk-availabilityzone"></a>
The AWS Region and Availability Zone location for the disk \(for example, `us-east-1a`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`DiskName`  <a name="cfn-lightsail-disk-diskname"></a>
The name of the disk\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\w[\w\-]*\w`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SizeInGb`  <a name="cfn-lightsail-disk-sizeingb"></a>
The size of the disk in GB\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: Updates are not supported\.

`Tags`  <a name="cfn-lightsail-disk-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation User Guide*\.  
The `Value` of `Tags` is optional for Lightsail resources\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lightsail-disk-return-values"></a>

### Ref<a name="aws-resource-lightsail-disk-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-lightsail-disk-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lightsail-disk-return-values-fn--getatt-fn--getatt"></a>

`AttachedTo`  <a name="AttachedTo-fn::getatt"></a>
The instance to which the disk is attached\.

`AttachmentState`  <a name="AttachmentState-fn::getatt"></a>
\(Deprecated\) The attachment state of the disk\.  
In releases prior to November 14, 2017, this parameter returned `attached` for system disks in the API response\. It is now deprecated, but still included in the response\. Use `isAttached` instead\.

`DiskArn`  <a name="DiskArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the disk\.

`Iops`  <a name="Iops-fn::getatt"></a>
The input/output operations per second \(IOPS\) of the disk\.

`IsAttached`  <a name="IsAttached-fn::getatt"></a>
A Boolean value indicating whether the disk is attached to an instance\.

`Location`  <a name="Location-fn::getatt"></a>
Property description not available\.

`Location.AvailabilityZone`  <a name="Location.AvailabilityZone-fn::getatt"></a>
Property description not available\.

`Location.RegionName`  <a name="Location.RegionName-fn::getatt"></a>
Property description not available\.

`Path`  <a name="Path-fn::getatt"></a>
The path of the disk\.

`ResourceType`  <a name="ResourceType-fn::getatt"></a>
The resource type of the disk \(for example, `Disk`\)\.

`State`  <a name="State-fn::getatt"></a>
The state of the disk \(for example, `in-use`\)\.

`SupportCode`  <a name="SupportCode-fn::getatt"></a>
The support code of the disk\.  
Include this code in your email to support when you have questions about a disk or another resource in Lightsail\. This code helps our support team to look up your Lightsail information\.

## Remarks<a name="aws-resource-lightsail-disk--remarks"></a>

*Availability Zone*

You can specify an Availability Zone when you perform a create disk request\. If you don’t specify one, the disk is created in the same Availability Zone as the last Lightsail resource you created\.

*Disk state*

Disks can be deleted only when they're in an `available` state\. If the disk is in an `attached` state when performing a delete disk request, the service will wait to check if the disk state changes to `available`\. The delete disk request times out if the disk state doesn't change to `available` within 15 minutes\.