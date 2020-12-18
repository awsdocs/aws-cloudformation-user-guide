# AWS::EC2::VPNGatewayRoutePropagation<a name="aws-resource-ec2-vpn-gatewayrouteprop"></a>

Enables a virtual private gateway \(VGW\) to propagate routes to the specified route table of a VPC\.

If you reference a VPN gateway that is in the same template as your VPN gateway route propagation, you must explicitly declare a dependency on the VPN gateway attachment\. The `AWS::EC2::VPNGatewayRoutePropagation` resource cannot use the VPN gateway until it has successfully attached to the VPC\. Add a [ DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) in the `AWS::EC2::VPNGatewayRoutePropagation` resource to explicitly declare a dependency on the VPN gateway attachment\.

## Syntax<a name="aws-resource-ec2-vpn-gatewayrouteprop-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpn-gatewayrouteprop-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPNGatewayRoutePropagation",
  "Properties" : {
      "[RouteTableIds](#cfn-ec2-vpngatewayrouteprop-routetableids)" : [ String, ... ],
      "[VpnGatewayId](#cfn-ec2-vpngatewayrouteprop-vpngatewayid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-vpn-gatewayrouteprop-syntax.yaml"></a>

```
Type: AWS::EC2::VPNGatewayRoutePropagation
Properties: 
  [RouteTableIds](#cfn-ec2-vpngatewayrouteprop-routetableids): 
    - String
  [VpnGatewayId](#cfn-ec2-vpngatewayrouteprop-vpngatewayid): String
```

## Properties<a name="aws-resource-ec2-vpn-gatewayrouteprop-properties"></a>

`RouteTableIds`  <a name="cfn-ec2-vpngatewayrouteprop-routetableids"></a>
The ID of the route table\. The routing table must be associated with the same VPC that the virtual private gateway is attached to\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpnGatewayId`  <a name="cfn-ec2-vpngatewayrouteprop-vpngatewayid"></a>
The ID of the virtual private gateway that is attached to a VPC\. The virtual private gateway must be attached to the same VPC that the routing tables are associated with\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-vpn-gatewayrouteprop-return-values"></a>

### Ref<a name="aws-resource-ec2-vpn-gatewayrouteprop-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPN gateway\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-vpn-gatewayrouteprop--examples"></a>



### VPN Gateway Route Propagation<a name="aws-resource-ec2-vpn-gatewayrouteprop--examples--VPN_Gateway_Route_Propagation"></a>

The following example enables route propagation for the private route table named PrivateRouteTable \.

#### JSON<a name="aws-resource-ec2-vpn-gatewayrouteprop--examples--VPN_Gateway_Route_Propagation--json"></a>

```
"myVPNGatewayRouteProp" : {
   "Type" : "AWS::EC2::VPNGatewayRoutePropagation",
   "Properties" : {
      "RouteTableIds" : [{"Ref" : "PrivateRouteTable"}],
      "VpnGatewayId" : {"Ref" : "VPNGateway"}
   }
}
```

#### YAML<a name="aws-resource-ec2-vpn-gatewayrouteprop--examples--VPN_Gateway_Route_Propagation--yaml"></a>

```
Type: AWS::EC2::VPNGatewayRoutePropagation
   Properties:
       RouteTableIds: 
        - !Ref PrivateRouteTable
       VpnGatewayId: !Ref VPNGateway
```

## See also<a name="aws-resource-ec2-vpn-gatewayrouteprop--seealso"></a>
+  [EnableVgwRoutePropagation](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_EnableVgwRoutePropagation.html) in the *Amazon EC2 API Reference*

