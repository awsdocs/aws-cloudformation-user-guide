# AWS::EC2::VPNGatewayRoutePropagation<a name="aws-resource-ec2-vpn-gatewayrouteprop"></a>

Enables a virtual private gateway \(VGW\) to propagate routes to the routing tables of a VPC\.

**Note**  
If you reference a VPN gateway that is in the same template as your VPN gateway route propagation, you must explicitly declare a dependency on the VPN gateway attachment\. The `AWS::EC2::VPNGatewayRoutePropagation` resource cannot use the VPN gateway until it has successfully attached to the VPC\. Add a [DependsOn](aws-attribute-dependson.md) attribute in the `AWS::EC2::VPNGatewayRoutePropagation` resource to explicitly declare a dependency on the VPN gateway attachment\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpngatewayroutepropagation-syntax)
+ [Properties](#w3ab2c21c10d551c11)
+ [Return Value](#w3ab2c21c10d551c13)
+ [Example](#w3ab2c21c10d551c15)
+ [See Also](#w3ab2c21c10d551c17)

## Syntax<a name="aws-resource-ec2-vpngatewayroutepropagation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpngatewayroutepropagation-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPNGatewayRoutePropagation",
   "Properties" : {
      "[RouteTableIds](#cfn-ec2-vpngatewayrouteprop-routetableids)" : [ String, ... ],
      "[VpnGatewayId](#cfn-ec2-vpngatewayrouteprop-vpngatewayid)" : String
   }
}
```

### YAML<a name="aws-resource-ec2-vpngatewayroutepropagation-syntax.yaml"></a>

```
Type: "AWS::EC2::VPNGatewayRoutePropagation"
Properties: 
  [RouteTableIds](#cfn-ec2-vpngatewayrouteprop-routetableids):
    - String
  [VpnGatewayId](#cfn-ec2-vpngatewayrouteprop-vpngatewayid): String
```

## Properties<a name="w3ab2c21c10d551c11"></a>

`RouteTableIds`  <a name="cfn-ec2-vpngatewayrouteprop-routetableids"></a>
A list of routing table IDs that are associated with a VPC\. The routing tables must be associated with the same VPC that the virtual private gateway is attached to\.  
*Required*: Yes  
*Type*: List of route table IDs  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpnGatewayId`  <a name="cfn-ec2-vpngatewayrouteprop-vpngatewayid"></a>
The ID of the virtual private gateway that is attached to a VPC\. The virtual private gateway must be attached to the same VPC that the routing tables are associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d551c13"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myVPNGatewayRouteProp" }
```

For the VPN gateway with the logical ID `myVPNGatewayRouteProp`, `Ref` will return the gateway's resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d551c15"></a>

### JSON<a name="aws-resource-ec2-vpngatewayroutepropagation-example.json"></a>

```
"myVPNGatewayRouteProp" : {
  "Type" : "AWS::EC2::VPNGatewayRoutePropagation",
  "Properties" : {
    "RouteTableIds" : [{"Ref" : "PrivateRouteTable"}],
    "VpnGatewayId" : {"Ref" : "VPNGateway"}
  }
}
```

### YAML<a name="aws-resource-ec2-vpngatewayroutepropagation-example.yaml"></a>

```
myVPNGatewayRouteProp: 
  Type: "AWS::EC2::VPNGatewayRoutePropagation"
  Properties:
    RouteTableIds: 
      - !Ref PrivateRouteTable
    VpnGatewayId: 
      !Ref VPNGateway
```

## See Also<a name="w3ab2c21c10d551c17"></a>
+ [EnableVgwRoutePropagation](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-EnableVgwRoutePropagation.html) in the *Amazon EC2 API Reference*\.