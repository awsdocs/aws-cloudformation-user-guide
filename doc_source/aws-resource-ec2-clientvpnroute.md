# AWS::EC2::ClientVpnRoute<a name="aws-resource-ec2-clientvpnroute"></a>

Specifies a network route to add to a Client VPN endpoint\. Each Client VPN endpoint has a route table that describes the available destination network routes\. Each route in the route table specifies the path for traffic to specific resources or networks\.

A target network association must be created before you can specify a route\. If you're setting up all the components of a Client VPN endpoint at the same time, you must use the [DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the `AWS::EC2::ClientVpnTargetNetworkAssociation` resource\.

## Syntax<a name="aws-resource-ec2-clientvpnroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-clientvpnroute-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::ClientVpnRoute",
  "Properties" : {
      "[ClientVpnEndpointId](#cfn-ec2-clientvpnroute-clientvpnendpointid)" : String,
      "[Description](#cfn-ec2-clientvpnroute-description)" : String,
      "[DestinationCidrBlock](#cfn-ec2-clientvpnroute-destinationcidrblock)" : String,
      "[TargetVpcSubnetId](#cfn-ec2-clientvpnroute-targetvpcsubnetid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-clientvpnroute-syntax.yaml"></a>

```
Type: AWS::EC2::ClientVpnRoute
Properties: 
  [ClientVpnEndpointId](#cfn-ec2-clientvpnroute-clientvpnendpointid): String
  [Description](#cfn-ec2-clientvpnroute-description): String
  [DestinationCidrBlock](#cfn-ec2-clientvpnroute-destinationcidrblock): String
  [TargetVpcSubnetId](#cfn-ec2-clientvpnroute-targetvpcsubnetid): String
```

## Properties<a name="aws-resource-ec2-clientvpnroute-properties"></a>

`ClientVpnEndpointId`  <a name="cfn-ec2-clientvpnroute-clientvpnendpointid"></a>
The ID of the Client VPN endpoint to which to add the route\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-clientvpnroute-description"></a>
A brief description of the route\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationCidrBlock`  <a name="cfn-ec2-clientvpnroute-destinationcidrblock"></a>
The IPv4 address range, in CIDR notation, of the route destination\. For example:  
+ To add a route for Internet access, enter `0.0.0.0/0` 
+ To add a route for a peered VPC, enter the peered VPC's IPv4 CIDR range
+ To add a route for an on\-premises network, enter the AWS Site\-to\-Site VPN connection's IPv4 CIDR range
+ To add a route for the local network, enter the client CIDR range
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetVpcSubnetId`  <a name="cfn-ec2-clientvpnroute-targetvpcsubnetid"></a>
The ID of the subnet through which you want to route traffic\. The specified subnet must be an existing target network of the Client VPN endpoint\.  
Alternatively, if you're adding a route for the local network, specify `local`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-ec2-clientvpnroute--examples"></a>

### Adding a route to a Client VPN endpoint<a name="aws-resource-ec2-clientvpnroute--examples--Adding_a_route_to_a_Client_VPN_endpoint"></a>

The following example adds a route for internet access to a Client VPN endpoint\.

#### YAML<a name="aws-resource-ec2-clientvpnroute--examples--Adding_a_route_to_a_Client_VPN_endpoint--yaml"></a>

```
myRoute:
  Type: "AWS::EC2::ClientVpnRoute"
  Properties:
    ClientVpnEndpointId: 
      Ref: myClientVpnEndpoint
    TargetVpcSubnetId: 
      Ref: mySubnet
    DestinationCidrBlock: "0.0.0.0/0"
    Description: "myRoute"
```

#### JSON<a name="aws-resource-ec2-clientvpnroute--examples--Adding_a_route_to_a_Client_VPN_endpoint--json"></a>

```
"myRoute": {
    "Type": "AWS::EC2::ClientVpnRoute",
    "Properties": {
        "ClientVpnEndpointId": {
            "Ref": "myClientVpnEndpoint"
        },
        "TargetVpcSubnetId": {
            "Ref": "mySubnet"
        },
        "DestinationCidrBlock": "0.0.0.0/0",
        "Description": "myRoute"
    }
}
```

## See also<a name="aws-resource-ec2-clientvpnroute--seealso"></a>
+ [Getting Started with Client VPN](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/cvpn-getting-started.html) in the *AWS Client VPN Administrator Guide*
+ [Routes](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/cvpn-working-routes.html) in the *AWS Client VPN Administrator Guide*

