# AWS::EC2::VPNConnection<a name="aws-resource-ec2-vpn-connection"></a>

Creates a new VPN connection between an existing virtual private gateway and a VPN customer gateway\.

For more information, see [CreateVpnConnection](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateVpnConnection.html) in the *Amazon EC2 API Reference*\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpnconnection-syntax)
+ [Properties](#w3ab2c21c10d537c11)
+ [Return Value](#w3ab2c21c10d537c13)
+ [Template Example](#w3ab2c21c10d537c15)
+ [See Also](#aws-resource-ec2-vpnconnection-seealso)

## Syntax<a name="aws-resource-ec2-vpnconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpnconnection-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::VPNConnection",
   "Properties" : {
      "[Type](#cfn-ec2-vpnconnection-type)" : String,
      "[CustomerGatewayId](#cfn-ec2-vpnconnection-customergatewayid)" : GatewayID,
      "[StaticRoutesOnly](#cfn-ec2-vpnconnection-StaticRoutesOnly)" : Boolean,
      "[Tags](#cfn-ec2-vpnconnection-tags)" :  [ Resource Tag, ... ],
      "[VpnGatewayId](#cfn-ec2-vpnconnection-vpngatewayid)" : GatewayID,
      "[VpnTunnelOptionsSpecifications](#cfn-ec2-vpnconnection-vpntunneloptionsspecifications)" : [ [*VpnTunnelOptionsSpecification*](aws-properties-ec2-vpnconnection-vpntunneloptionsspecification.md), ... ]
   }
}
```

### YAML<a name="aws-resource-ec2-vpnconnection-syntax.yaml"></a>

```
Type: "AWS::EC2::VPNConnection"
Properties: 
  [Type](#cfn-ec2-vpnconnection-type): String
  [CustomerGatewayId](#cfn-ec2-vpnconnection-customergatewayid):
    GatewayID
  [StaticRoutesOnly](#cfn-ec2-vpnconnection-StaticRoutesOnly): Boolean
  [Tags](#cfn-ec2-vpnconnection-tags):
    - Resource Tag
  [VpnGatewayId](#cfn-ec2-vpnconnection-vpngatewayid):
    GatewayID
  [VpnTunnelOptionsSpecifications](#cfn-ec2-vpnconnection-vpntunneloptionsspecifications): 
    - [*VpnTunnelOptionsSpecification*](aws-properties-ec2-vpnconnection-vpntunneloptionsspecification.md)
```

## Properties<a name="w3ab2c21c10d537c11"></a>

`Type`  <a name="cfn-ec2-vpnconnection-type"></a>
The type of VPN connection this virtual private gateway supports\.  
Example: "ipsec\.1"  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CustomerGatewayId`  <a name="cfn-ec2-vpnconnection-customergatewayid"></a>
The ID of the customer gateway\. This can either be an embedded JSON object or a reference to a Gateway ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`StaticRoutesOnly`  <a name="cfn-ec2-vpnconnection-StaticRoutesOnly"></a>
Indicates whether the VPN connection requires static routes\.  
*Required*: Conditional\. If you are creating a VPN connection for a device that does not support Border Gateway Protocol \(BGP\), you must specify `true`\.  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-ec2-vpnconnection-tags"></a>
The tags that you want to attach to the resource\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VpnGatewayId`  <a name="cfn-ec2-vpnconnection-vpngatewayid"></a>
The ID of the virtual private gateway\. This can either be an embedded JSON object or a reference to a Gateway ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VpnTunnelOptionsSpecifications`  <a name="cfn-ec2-vpnconnection-vpntunneloptionsspecifications"></a>
The tunnel options for the VPN connection\. Duplicates not allowed\.  
 *Required*: No  
 *Type*: List of [EC2 VPNConnection VpnTunnelOptionsSpecification](aws-properties-ec2-vpnconnection-vpntunneloptionsspecification.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Value<a name="w3ab2c21c10d537c13"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyVPNConnection" }
```

For the VPNConnection with the logical ID "MyVPNConnection", `Ref` will return the VPN connection's resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Template Example<a name="w3ab2c21c10d537c15"></a>

### JSON<a name="aws-resource-ec2-vpnconnection-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myVPNConnection" : {
         "Type" : "AWS::EC2::VPNConnection",
         "Properties" : {
            "Type" : "ipsec.1",
    	    "StaticRoutesOnly" : "true",
            "CustomerGatewayId" : {"Ref" : "myCustomerGateway"},
            "VpnGatewayId" : {"Ref" : "myVPNGateway"}
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-vpnconnection-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources:
  myVPNConnection: 
    Type: "AWS::EC2::VPNConnection"
    Properties: 
      Type: ipsec.1
      StaticRoutesOnly: true
      CustomerGatewayId: 
        !Ref myCustomerGateway
      VpnGatewayId: 
        !Ref myVPNGateway
```

## See Also<a name="aws-resource-ec2-vpnconnection-seealso"></a>
+  [VpnConnection](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_VpnConnection.html) in the *Amazon EC2 API Reference*