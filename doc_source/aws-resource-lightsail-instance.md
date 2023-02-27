# AWS::Lightsail::Instance<a name="aws-resource-lightsail-instance"></a>

The `AWS::Lightsail::Instance` resource specifies an Amazon Lightsail instance\.

## Syntax<a name="aws-resource-lightsail-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lightsail-instance-syntax.json"></a>

```
{
  "Type" : "AWS::Lightsail::Instance",
  "Properties" : {
      "[AddOns](#cfn-lightsail-instance-addons)" : [ AddOn, ... ],
      "[AvailabilityZone](#cfn-lightsail-instance-availabilityzone)" : String,
      "[BlueprintId](#cfn-lightsail-instance-blueprintid)" : String,
      "[BundleId](#cfn-lightsail-instance-bundleid)" : String,
      "[Hardware](#cfn-lightsail-instance-hardware)" : Hardware,
      "[InstanceName](#cfn-lightsail-instance-instancename)" : String,
      "[KeyPairName](#cfn-lightsail-instance-keypairname)" : String,
      "[Location](#cfn-lightsail-instance-location)" : Location,
      "[Networking](#cfn-lightsail-instance-networking)" : Networking,
      "[State](#cfn-lightsail-instance-state)" : State,
      "[Tags](#cfn-lightsail-instance-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserData](#cfn-lightsail-instance-userdata)" : String
    }
}
```

### YAML<a name="aws-resource-lightsail-instance-syntax.yaml"></a>

```
Type: AWS::Lightsail::Instance
Properties: 
  [AddOns](#cfn-lightsail-instance-addons): 
    - AddOn
  [AvailabilityZone](#cfn-lightsail-instance-availabilityzone): String
  [BlueprintId](#cfn-lightsail-instance-blueprintid): String
  [BundleId](#cfn-lightsail-instance-bundleid): String
  [Hardware](#cfn-lightsail-instance-hardware): 
    Hardware
  [InstanceName](#cfn-lightsail-instance-instancename): String
  [KeyPairName](#cfn-lightsail-instance-keypairname): String
  [Location](#cfn-lightsail-instance-location): 
    Location
  [Networking](#cfn-lightsail-instance-networking): 
    Networking
  [State](#cfn-lightsail-instance-state): 
    State
  [Tags](#cfn-lightsail-instance-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserData](#cfn-lightsail-instance-userdata): String
```

## Properties<a name="aws-resource-lightsail-instance-properties"></a>

`AddOns`  <a name="cfn-lightsail-instance-addons"></a>
An array of add\-ons for the instance\.  
If the instance has an add\-on enabled when performing a delete instance request, the add\-on is automatically disabled before the instance is deleted\.
*Required*: No  
*Type*: List of [AddOn](aws-properties-lightsail-instance-addon.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-lightsail-instance-availabilityzone"></a>
The Availability Zone for the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`BlueprintId`  <a name="cfn-lightsail-instance-blueprintid"></a>
The blueprint ID for the instance \(for example, `os_amlinux_2016_03`\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`BundleId`  <a name="cfn-lightsail-instance-bundleid"></a>
The bundle ID for the instance \(for example, `micro_1_0`\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Hardware`  <a name="cfn-lightsail-instance-hardware"></a>
The hardware properties for the instance, such as the vCPU count, attached disks, and amount of RAM\.  
The instance restarts when performing an attach disk or detach disk request\. This resets the public IP address of your instance if a static IP isn't attached to it\.
*Required*: No  
*Type*: [Hardware](aws-properties-lightsail-instance-hardware.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`InstanceName`  <a name="cfn-lightsail-instance-instancename"></a>
The name of the instance\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\w[\w\-]*\w`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyPairName`  <a name="cfn-lightsail-instance-keypairname"></a>
The name of the key pair to use for the instance\.  
If no key pair name is specified, the Regional Lightsail default key pair is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Location`  <a name="cfn-lightsail-instance-location"></a>
The location for the instance, such as the AWS Region and Availability Zone\.  
The `Location` property is read\-only and should not be specified in a create instance or update instance request\.
*Required*: No  
*Type*: [Location](aws-properties-lightsail-instance-location.md)  
*Update requires*: Updates are not supported\.

`Networking`  <a name="cfn-lightsail-instance-networking"></a>
The public ports and the monthly amount of data transfer allocated for the instance\.  
*Required*: No  
*Type*: [Networking](aws-properties-lightsail-instance-networking.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-lightsail-instance-state"></a>
The status code and the state \(for example, `running`\) of the instance\.  
The `State` property is read\-only and should not be specified in a create instance or update instance request\.
*Required*: No  
*Type*: [State](aws-properties-lightsail-instance-state.md)  
*Update requires*: Updates are not supported\.

`Tags`  <a name="cfn-lightsail-instance-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation User Guide*\.  
The `Value` of `Tags` is optional for Lightsail resources\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserData`  <a name="cfn-lightsail-instance-userdata"></a>
The optional launch script for the instance\.  
Specify a launch script to configure an instance with additional user data\. For example, you might want to specify `apt-get -y update` as a launch script\.  
Depending on the blueprint of your instance, the command to get software on your instance varies\. Amazon Linux and CentOS use `yum`, Debian and Ubuntu use `apt-get`, and FreeBSD uses `pkg`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lightsail-instance-return-values"></a>

### Ref<a name="aws-resource-lightsail-instance-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-lightsail-instance-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lightsail-instance-return-values-fn--getatt-fn--getatt"></a>

`Hardware.CpuCount`  <a name="Hardware.CpuCount-fn::getatt"></a>
The number of vCPUs the instance has\.

`Hardware.RamSizeInGb`  <a name="Hardware.RamSizeInGb-fn::getatt"></a>
The amount of RAM in GB on the instance \(for example, `1.0`\)\.

`InstanceArn`  <a name="InstanceArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the instance \(for example, `arn:aws:lightsail:us-east-2:123456789101:Instance/244ad76f-8aad-4741-809f-12345EXAMPLE`\)\.

`IsStaticIp`  <a name="IsStaticIp-fn::getatt"></a>
A Boolean value indicating whether the instance has a static IP assigned to it\.

`Location.AvailabilityZone`  <a name="Location.AvailabilityZone-fn::getatt"></a>
The AWS Region and Availability Zone where the instance is located\.

`Location.RegionName`  <a name="Location.RegionName-fn::getatt"></a>
The AWS Region of the instance\.

`Networking.MonthlyTransfer.GbPerMonthAllocated`  <a name="Networking.MonthlyTransfer.GbPerMonthAllocated-fn::getatt"></a>
The amount of allocated monthly data transfer \(in GB\) for an instance\.

`PrivateIpAddress`  <a name="PrivateIpAddress-fn::getatt"></a>
The private IP address of the instance\.

`PublicIpAddress`  <a name="PublicIpAddress-fn::getatt"></a>
The public IP address of the instance\.

`ResourceType`  <a name="ResourceType-fn::getatt"></a>
The resource type of the instance \(for example, `Instance`\)\.

`SshKeyName`  <a name="SshKeyName-fn::getatt"></a>
The name of the SSH key pair used by the instance\.

`State.Code`  <a name="State.Code-fn::getatt"></a>
The status code of the instance\.

`State.Name`  <a name="State.Name-fn::getatt"></a>
The state of the instance \(for example, `running` or `pending`\)\.

`SupportCode`  <a name="SupportCode-fn::getatt"></a>
The support code of the instance\.  
Include this code in your email to support when you have questions about an instance or another resource in Lightsail\. This code helps our support team to look up your Lightsail information\.

`UserName`  <a name="UserName-fn::getatt"></a>
The user name for connecting to the instance \(for example, `ec2-user`\)\.

## Remarks<a name="aws-resource-lightsail-instance--remarks"></a>

*Attaching a static IP to an instance*

You cannot attach a static IP to an instance using the instance resource\. Instead, you must use the static IP resource to attach a static IP to an instance\. To attach a static IP to an instance, the instance must be in a `running` state\.

*Network ports*

If no network ports are specified when performing a create instance request, the default network ports are opened when the instance is created\.

To open ports on your instance when performing a create instance request, you must specify all the ports that you want to open, including the default ports\. The default ports are not automatically opened when you specify the ports you want to open\.

*Disk attach and detach*

The instance restarts when performing an attach disk or detach disk request\. This resets the public IP address of your instance if a static IP isn't attached to it\.

If you detach a disk \(for eample, `DiskA`\) and attach a different disk \(for example, `DiskB`\) in the same request, and the attach disk request fails, AWS CloudFormation will attempt to roll back the changes so that `DiskA` is re\-attached to the instance\. However, if you delete `DiskA` before AWS CloudFormation attemps the roll\-back, then the roll\-back will fail and the instance will not have either disk attached\.

*Read\-only properties*

The `State`, `Location`, `CpuCount`, and `RamSizeInGb` properties are read\-only and should not be specified in a create instance or update instance request\.