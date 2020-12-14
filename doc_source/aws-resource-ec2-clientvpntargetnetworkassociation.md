# AWS::EC2::ClientVpnTargetNetworkAssociation<a name="aws-resource-ec2-clientvpntargetnetworkassociation"></a>

Specifies a target network to associate with a Client VPN endpoint\. A target network is a subnet in a VPC\. You can associate multiple subnets from the same VPC with a Client VPN endpoint\. You can associate only one subnet in each Availability Zone\. We recommend that you associate at least two subnets to provide Availability Zone redundancy\.

## Syntax<a name="aws-resource-ec2-clientvpntargetnetworkassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-clientvpntargetnetworkassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::ClientVpnTargetNetworkAssociation",
  "Properties" : {
      "[ClientVpnEndpointId](#cfn-ec2-clientvpntargetnetworkassociation-clientvpnendpointid)" : String,
      "[SubnetId](#cfn-ec2-clientvpntargetnetworkassociation-subnetid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-clientvpntargetnetworkassociation-syntax.yaml"></a>

```
Type: AWS::EC2::ClientVpnTargetNetworkAssociation
Properties: 
  [ClientVpnEndpointId](#cfn-ec2-clientvpntargetnetworkassociation-clientvpnendpointid): String
  [SubnetId](#cfn-ec2-clientvpntargetnetworkassociation-subnetid): String
```

## Properties<a name="aws-resource-ec2-clientvpntargetnetworkassociation-properties"></a>

`ClientVpnEndpointId`  <a name="cfn-ec2-clientvpntargetnetworkassociation-clientvpnendpointid"></a>
The ID of the Client VPN endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-ec2-clientvpntargetnetworkassociation-subnetid"></a>
The ID of the subnet to associate with the Client VPN endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-clientvpntargetnetworkassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-clientvpntargetnetworkassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the association ID\. For example: `cvpn-assoc-1234567890abcdef0`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-clientvpntargetnetworkassociation--examples"></a>

### Associating a target subnet with a Client VPN endpoint<a name="aws-resource-ec2-clientvpntargetnetworkassociation--examples--Associating_a_target_subnet_with_a_Client_VPN_endpoint"></a>

The following example associates a target network with a Client VPN endpoint\.

#### YAML<a name="aws-resource-ec2-clientvpntargetnetworkassociation--examples--Associating_a_target_subnet_with_a_Client_VPN_endpoint--yaml"></a>

```
myNetworkAssociation:
  Type: "AWS::EC2::ClientVpnTargetNetworkAssociation"
  Properties:
    ClientVpnEndpointId: 
      Ref: myClientVpnEndpoint
    SubnetId: 
      Ref: mySubnet
```

#### JSON<a name="aws-resource-ec2-clientvpntargetnetworkassociation--examples--Associating_a_target_subnet_with_a_Client_VPN_endpoint--json"></a>

```
"myNetworkAssociation": {
    "Type": "AWS::EC2::ClientVpnTargetNetworkAssociation",
    "Properties": {
        "ClientVpnEndpointId": {
            "Ref": "myClientVpnEndpoint"
        },
        "SubnetId": {
            "Ref": "mySubnet"
        }
    }
}
```

## See also<a name="aws-resource-ec2-clientvpntargetnetworkassociation--seealso"></a>
+ [ Getting Started with Client VPN](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/cvpn-getting-started.html) in the *AWS Client VPN Administrator Guide*
+ [Target Networks](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/cvpn-working-target.html) in the *AWS Client VPN Administrator Guide*

