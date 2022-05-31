# AWS::EC2::TransitGatewayMulticastGroupSource<a name="aws-resource-ec2-transitgatewaymulticastgroupsource"></a>

Registers sources \(network interfaces\) with the specified transit gateway multicast domain\.

A multicast source is a network interface attached to a supported instance that sends multicast traffic\. For information about supported instances, see [Multicast Considerations](https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-limits.html#multicast-limits) in *Amazon VPC Transit Gateways*\.

## Syntax<a name="aws-resource-ec2-transitgatewaymulticastgroupsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-transitgatewaymulticastgroupsource-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::TransitGatewayMulticastGroupSource",
  "Properties" : {
      "[GroupIpAddress](#cfn-ec2-transitgatewaymulticastgroupsource-groupipaddress)" : String,
      "[NetworkInterfaceId](#cfn-ec2-transitgatewaymulticastgroupsource-networkinterfaceid)" : String,
      "[TransitGatewayMulticastDomainId](#cfn-ec2-transitgatewaymulticastgroupsource-transitgatewaymulticastdomainid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-transitgatewaymulticastgroupsource-syntax.yaml"></a>

```
Type: AWS::EC2::TransitGatewayMulticastGroupSource
Properties: 
  [GroupIpAddress](#cfn-ec2-transitgatewaymulticastgroupsource-groupipaddress): String
  [NetworkInterfaceId](#cfn-ec2-transitgatewaymulticastgroupsource-networkinterfaceid): String
  [TransitGatewayMulticastDomainId](#cfn-ec2-transitgatewaymulticastgroupsource-transitgatewaymulticastdomainid): String
```

## Properties<a name="aws-resource-ec2-transitgatewaymulticastgroupsource-properties"></a>

`GroupIpAddress`  <a name="cfn-ec2-transitgatewaymulticastgroupsource-groupipaddress"></a>
The IP address assigned to the transit gateway multicast group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkInterfaceId`  <a name="cfn-ec2-transitgatewaymulticastgroupsource-networkinterfaceid"></a>
The group sources' network interface IDs to register with the transit gateway multicast group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayMulticastDomainId`  <a name="cfn-ec2-transitgatewaymulticastgroupsource-transitgatewaymulticastdomainid"></a>
The ID of the transit gateway multicast domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-transitgatewaymulticastgroupsource-return-values"></a>

### Ref<a name="aws-resource-ec2-transitgatewaymulticastgroupsource-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the transit gateway multicast domain group source\. 

### Fn::GetAtt<a name="aws-resource-ec2-transitgatewaymulticastgroupsource-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-transitgatewaymulticastgroupsource-return-values-fn--getatt-fn--getatt"></a>

`GroupMember`  <a name="GroupMember-fn::getatt"></a>
Information about the registered transit gateway multicast domain group members\.

`GroupSource`  <a name="GroupSource-fn::getatt"></a>
Indicates that the resource is a transit gateway group member\.

`MemberType`  <a name="MemberType-fn::getatt"></a>
The type of group member, for example static\.

`ResourceId`  <a name="ResourceId-fn::getatt"></a>
The ID of the resource\.

`ResourceType`  <a name="ResourceType-fn::getatt"></a>
The type of resource, for example a VPC attachment\.

`SourceType`  <a name="SourceType-fn::getatt"></a>
The type of source\.

`SubnetId`  <a name="SubnetId-fn::getatt"></a>
The ID of the subnet\.

`TransitGatewayAttachmentId`  <a name="TransitGatewayAttachmentId-fn::getatt"></a>
The ID of the transit gateway attachment\.

## See also<a name="aws-resource-ec2-transitgatewaymulticastgroupsource--seealso"></a>
+ [RegisterTransitGatewayMulticastGroupSources](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_RegisterTransitGatewayMulticastGroupSources.html) in the *Amazon EC2 API Reference*

