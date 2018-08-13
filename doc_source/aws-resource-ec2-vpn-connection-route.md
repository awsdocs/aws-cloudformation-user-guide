# AWS::EC2::VPNConnectionRoute<a name="aws-resource-ec2-vpn-connection-route"></a>

A static route that is associated with a VPN connection between an existing virtual private gateway and a VPN customer gateway\. The static route allows traffic to be routed from the virtual private gateway to the VPN customer gateway\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpnconnectionroute-syntax)
+ [Properties](#w3ab2c21c10d541b9)
+ [Return Values](#w3ab2c21c10d541c11)
+ [Example](#w3ab2c21c10d541c13)
+ [See Also](#w3ab2c21c10d541c15)

## Syntax<a name="aws-resource-ec2-vpnconnectionroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpnconnectionroute-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPNConnectionRoute",
   "Properties" : {
      "[DestinationCidrBlock](#cfn-ec2-vpnconnectionroute-cidrblock)" : String,
      "[VpnConnectionId](#cfn-ec2-vpnconnectionroute-connectionid)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-vpnconnectionroute-syntax.yaml"></a>

```
Type: "AWS::EC2::VPNConnectionRoute"
Properties: 
  [DestinationCidrBlock](#cfn-ec2-vpnconnectionroute-cidrblock): String
  [VpnConnectionId](#cfn-ec2-vpnconnectionroute-connectionid): String
```

## Properties<a name="w3ab2c21c10d541b9"></a>

`DestinationCidrBlock`  <a name="cfn-ec2-vpnconnectionroute-cidrblock"></a>
The CIDR block that is associated with the local subnet of the customer network\.  
*Required*: Yes\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VpnConnectionId`  <a name="cfn-ec2-vpnconnectionroute-connectionid"></a>
The ID of the VPN connection\.  
*Required*: Yes\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d541c11"></a>

### Ref<a name="w3ab2c21c10d541c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d541c13"></a>

### JSON<a name="aws-resource-ec2-vpnconnectionroute-example.json"></a>

```
"MyConnectionRoute0" : {
   "Type" : "AWS::EC2::VPNConnectionRoute",
   "Properties" : {
      "DestinationCidrBlock" : "10.0.0.0/16",
      "VpnConnectionId" : {"Ref" : "Connection0"}
   }
}
```

### YAML<a name="aws-resource-ec2-vpnconnectionroute-example.yaml"></a>

```
MyConnectionRoute0: 
  Type: "AWS::EC2::VPNConnectionRoute"
  Properties: 
    DestinationCidrBlock: 10.0.0.0/16
    VpnConnectionId: 
      !Ref Connection0
```

## See Also<a name="w3ab2c21c10d541c15"></a>
+ [CreateVpnConnectionRoute](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVpnConnectionRoute.html) in the *Amazon EC2 API Reference*\.