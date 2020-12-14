# AWS::EC2::VPNConnectionRoute<a name="aws-resource-ec2-vpn-connection-route"></a>

Specifies a static route for a VPN connection between an existing virtual private gateway and a VPN customer gateway\. The static route allows traffic to be routed from the virtual private gateway to the VPN customer gateway\.

For more information, see [AWS Site\-to\-Site VPN](https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html) in the *AWS Site\-to\-Site VPN User Guide*\.

## Syntax<a name="aws-resource-ec2-vpn-connection-route-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpn-connection-route-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPNConnectionRoute",
  "Properties" : {
      "[DestinationCidrBlock](#cfn-ec2-vpnconnectionroute-cidrblock)" : String,
      "[VpnConnectionId](#cfn-ec2-vpnconnectionroute-connectionid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-vpn-connection-route-syntax.yaml"></a>

```
Type: AWS::EC2::VPNConnectionRoute
Properties: 
  [DestinationCidrBlock](#cfn-ec2-vpnconnectionroute-cidrblock): String
  [VpnConnectionId](#cfn-ec2-vpnconnectionroute-connectionid): String
```

## Properties<a name="aws-resource-ec2-vpn-connection-route-properties"></a>

`DestinationCidrBlock`  <a name="cfn-ec2-vpnconnectionroute-cidrblock"></a>
The CIDR block associated with the local subnet of the customer network\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpnConnectionId`  <a name="cfn-ec2-vpnconnectionroute-connectionid"></a>
The ID of the VPN connection\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpn-connection-route-return-values"></a>

### Ref<a name="aws-resource-ec2-vpn-connection-route-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPN connection route\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-vpn-connection-route--examples"></a>



### VPN Connection Route<a name="aws-resource-ec2-vpn-connection-route--examples--VPN_Connection_Route"></a>

The following example specifies a VPN connection route\.

#### JSON<a name="aws-resource-ec2-vpn-connection-route--examples--VPN_Connection_Route--json"></a>

```
"MyConnectionRoute0" : {
   "Type" : "AWS::EC2::VPNConnectionRoute",
    "Properties" : {
       "DestinationCidrBlock" : "10.0.0.0/16",
       "VpnConnectionId" : {"Ref" : "Connection0"}
    }
}
```

#### YAML<a name="aws-resource-ec2-vpn-connection-route--examples--VPN_Connection_Route--yaml"></a>

```
MyConnectionRoute0: 
  Type: AWS::EC2::VPNConnectionRoute
  Properties: 
     DestinationCidrBlock: 10.0.0.0/16
     VpnConnectionId: 
     !Ref Connection0
```

## See also<a name="aws-resource-ec2-vpn-connection-route--seealso"></a>
+  [CreateVpnConnectionRoute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVpnConnectionRoute.html) in the *Amazon EC2 API Reference*

