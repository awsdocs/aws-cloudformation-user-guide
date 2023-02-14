# AWS::MediaLive::Channel VpcOutputSettings<a name="aws-properties-medialive-channel-vpcoutputsettings"></a>

Settings to enable VPC mode in the channel, so that the endpoints for all outputs are in your VPC\.

This entity is at the top level in the channel\.

## Syntax<a name="aws-properties-medialive-channel-vpcoutputsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-vpcoutputsettings-syntax.json"></a>

```
{
  "[PublicAddressAllocationIds](#cfn-medialive-channel-vpcoutputsettings-publicaddressallocationids)" : [ String, ... ],
  "[SecurityGroupIds](#cfn-medialive-channel-vpcoutputsettings-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-medialive-channel-vpcoutputsettings-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-medialive-channel-vpcoutputsettings-syntax.yaml"></a>

```
  [PublicAddressAllocationIds](#cfn-medialive-channel-vpcoutputsettings-publicaddressallocationids): 
    - String
  [SecurityGroupIds](#cfn-medialive-channel-vpcoutputsettings-securitygroupids): 
    - String
  [SubnetIds](#cfn-medialive-channel-vpcoutputsettings-subnetids): 
    - String
```

## Properties<a name="aws-properties-medialive-channel-vpcoutputsettings-properties"></a>

`PublicAddressAllocationIds`  <a name="cfn-medialive-channel-vpcoutputsettings-publicaddressallocationids"></a>
List of public address allocation IDs to associate with ENIs that will be created in Output VPC\. Must specify one for SINGLE\_PIPELINE, two for STANDARD channels   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-medialive-channel-vpcoutputsettings-securitygroupids"></a>
A list of up to 5 EC2 VPC security group IDs to attach to the Output VPC network interfaces\. If none are specified then the VPC default security group will be used   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-medialive-channel-vpcoutputsettings-subnetids"></a>
A list of VPC subnet IDs from the same VPC\. If STANDARD channel, subnet IDs must be mapped to two unique availability zones \(AZ\)\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)