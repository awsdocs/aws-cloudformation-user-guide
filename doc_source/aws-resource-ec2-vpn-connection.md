# AWS::EC2::VPNConnection<a name="aws-resource-ec2-vpn-connection"></a>

Specifies a VPN connection between a virtual private gateway and a VPN customer gateway or a transit gateway and a VPN customer gateway\.

To specify a VPN connection between a transit gateway and customer gateway, use the `TransitGatewayId` and `CustomerGatewayId` properties\.

To specify a VPN connection between a virtual private gateway and customer gateway, use the `VpnGatewayId` and `CustomerGatewayId` properties\.

For more information, see [AWS Site\-to\-Site VPN](https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html) in the *AWS Site\-to\-Site VPN User Guide*\.

## Syntax<a name="aws-resource-ec2-vpn-connection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpn-connection-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPNConnection",
  "Properties" : {
      "[CustomerGatewayId](#cfn-ec2-vpnconnection-customergatewayid)" : String,
      "[StaticRoutesOnly](#cfn-ec2-vpnconnection-StaticRoutesOnly)" : Boolean,
      "[Tags](#cfn-ec2-vpnconnection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TransitGatewayId](#cfn-ec2-vpnconnection-transitgatewayid)" : String,
      "[Type](#cfn-ec2-vpnconnection-type)" : String,
      "[VpnGatewayId](#cfn-ec2-vpnconnection-vpngatewayid)" : String,
      "[VpnTunnelOptionsSpecifications](#cfn-ec2-vpnconnection-vpntunneloptionsspecifications)" : [ VpnTunnelOptionsSpecification, ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-vpn-connection-syntax.yaml"></a>

```
Type: AWS::EC2::VPNConnection
Properties: 
  [CustomerGatewayId](#cfn-ec2-vpnconnection-customergatewayid): String
  [StaticRoutesOnly](#cfn-ec2-vpnconnection-StaticRoutesOnly): Boolean
  [Tags](#cfn-ec2-vpnconnection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TransitGatewayId](#cfn-ec2-vpnconnection-transitgatewayid): String
  [Type](#cfn-ec2-vpnconnection-type): String
  [VpnGatewayId](#cfn-ec2-vpnconnection-vpngatewayid): String
  [VpnTunnelOptionsSpecifications](#cfn-ec2-vpnconnection-vpntunneloptionsspecifications): 
    - VpnTunnelOptionsSpecification
```

## Properties<a name="aws-resource-ec2-vpn-connection-properties"></a>

`CustomerGatewayId`  <a name="cfn-ec2-vpnconnection-customergatewayid"></a>
The ID of the customer gateway at your end of the VPN connection\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StaticRoutesOnly`  <a name="cfn-ec2-vpnconnection-StaticRoutesOnly"></a>
Indicates whether the VPN connection uses static routes only\. Static routes must be used for devices that don't support BGP\.  
If you are creating a VPN connection for a device that does not support Border Gateway Protocol \(BGP\), you must specify `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-vpnconnection-tags"></a>
Any tags assigned to the VPN connection\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGatewayId`  <a name="cfn-ec2-vpnconnection-transitgatewayid"></a>
The ID of the transit gateway associated with the VPN connection\.  
You must specify either `TransitGatewayId` or `VpnGatewayId`, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-ec2-vpnconnection-type"></a>
The type of VPN connection\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ipsec.1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpnGatewayId`  <a name="cfn-ec2-vpnconnection-vpngatewayid"></a>
The ID of the virtual private gateway at the AWS side of the VPN connection\.  
You must specify either `TransitGatewayId` or `VpnGatewayId`, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpnTunnelOptionsSpecifications`  <a name="cfn-ec2-vpnconnection-vpntunneloptionsspecifications"></a>
The tunnel options for the VPN connection\.  
*Required*: No  
*Type*: List of [VpnTunnelOptionsSpecification](aws-properties-ec2-vpnconnection-vpntunneloptionsspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpn-connection-return-values"></a>

### Ref<a name="aws-resource-ec2-vpn-connection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPN connection\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-vpn-connection--examples"></a>



### VPN Connection<a name="aws-resource-ec2-vpn-connection--examples--VPN_Connection"></a>

The following example specifies a VPN connection between myVPNGateway and MyCustomerGateway\.

#### JSON<a name="aws-resource-ec2-vpn-connection--examples--VPN_Connection--json"></a>

```
"myVPNConnection" : {
   "Type" : "AWS::EC2::VPNConnection",
   "Properties" : {
      "Type" : "ipsec.1",
      "StaticRoutesOnly" : "true",
      "CustomerGatewayId" : {"Ref" : "myCustomerGateway"},
      "VpnGatewayId" : {"Ref" : "myVPNGateway"}
   }
}
```

#### YAML<a name="aws-resource-ec2-vpn-connection--examples--VPN_Connection--yaml"></a>

```
   myVPNConnection: 
      Type: AWS::EC2::VPNConnection
      Properties: 
        Type: ipsec.1
        StaticRoutesOnly: true
        CustomerGatewayId: 
          !Ref myCustomerGateway
        VpnGatewayId: 
          !Ref myVPNGateway
```

## See also<a name="aws-resource-ec2-vpn-connection--seealso"></a>
+  [VPNConnection](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_VpnConnection.html) in the *Amazon EC2 API Reference*

