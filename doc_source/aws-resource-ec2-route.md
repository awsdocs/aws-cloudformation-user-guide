# AWS::EC2::Route<a name="aws-resource-ec2-route"></a>

The `AWS::EC2::Route` resource creates a new route in a route table within a VPC\. The route's target can be either a gateway attached to the VPC or a NAT instance in the VPC\.

**Topics**
+ [Syntax](#aws-resource-ec2-route-syntax)
+ [Properties](#w3ab2c21c10d454b9)
+ [Return Values](#w3ab2c21c10d454c11)
+ [Examples](#w3ab2c21c10d454c13)
+ [More Info](#w3ab2c21c10d454c15)

## Syntax<a name="aws-resource-ec2-route-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-route-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Route",
  "Properties" : {
    "[DestinationCidrBlock](#cfn-ec2-route-destinationcidrblock)" : String,
    "[DestinationIpv6CidrBlock](#cfn-ec2-route-destinationipv6cidrblock)" : String,
    "[EgressOnlyInternetGatewayId](#cfn-ec2-route-egressonlyinternetgatewayid)" : String,
    "[GatewayId](#cfn-ec2-route-gatewayid)" : String,
    "[InstanceId](#cfn-ec2-route-instanceid)" : String,
    "[NatGatewayId](#cfn-ec2-route-natgatewayid)" : String,
    "[NetworkInterfaceId](#cfn-ec2-route-networkinterfaceid)" : String,
    "[RouteTableId](#cfn-ec2-route-routetableid)" : String,
    "[VpcPeeringConnectionId](#cfn-ec2-route-vpcpeeringconnectionid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-route-syntax.yaml"></a>

```
Type: "AWS::EC2::Route"
Properties: 
  [DestinationCidrBlock](#cfn-ec2-route-destinationcidrblock): String
  [DestinationIpv6CidrBlock](#cfn-ec2-route-destinationipv6cidrblock): String
  [EgressOnlyInternetGatewayId](#cfn-ec2-route-egressonlyinternetgatewayid): String
  [GatewayId](#cfn-ec2-route-gatewayid): String
  [InstanceId](#cfn-ec2-route-instanceid): String
  [NatGatewayId](#cfn-ec2-route-natgatewayid): String
  [NetworkInterfaceId](#cfn-ec2-route-networkinterfaceid): String
  [RouteTableId](#cfn-ec2-route-routetableid): String
  [VpcPeeringConnectionId](#cfn-ec2-route-vpcpeeringconnectionid): String
```

## Properties<a name="w3ab2c21c10d454b9"></a>

`DestinationCidrBlock`  <a name="cfn-ec2-route-destinationcidrblock"></a>
The IPv4 CIDR address block used for the destination match\. For example, `0.0.0.0/0`\. Routing decisions are based on the most specific match\.  
*Required*: Conditional\. You must specify the `DestinationCidrBlock` or `DestinationIpv6CidrBlock` property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DestinationIpv6CidrBlock`  <a name="cfn-ec2-route-destinationipv6cidrblock"></a>
The IPv6 CIDR address block used for the destination match\. For example, `::/0`\. Routing decisions are based on the most specific match\.  
*Required*: Conditional\. You must specify the `DestinationCidrBlock` or `DestinationIpv6CidrBlock` property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EgressOnlyInternetGatewayId`  <a name="cfn-ec2-route-egressonlyinternetgatewayid"></a>
The ID of an egress\-only internet gateway that is attached to your VPC \(over IPv6 only\)\.  
*Required*: Conditional\. You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\. For an example that uses this property, see [Amazon EC2 Route with Egress\-Only Internet Gateway](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-ec2.html#quickref-ec2-route-egressonlyinternetgateway)\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`GatewayId`  <a name="cfn-ec2-route-gatewayid"></a>
The ID of an internet gateway or virtual private gateway that is attached to your VPC\. For example: `igw-eaad4883`\.  
For route entries that specify a gateway, you must specify a dependency on the gateway attachment resource\. For more information, see [DependsOn Attribute](aws-attribute-dependson.md)\.  
*Required*: Conditional\. You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceId`  <a name="cfn-ec2-route-instanceid"></a>
The ID of a NAT instance in your VPC\. For example, `i-1a2b3c4d`\.  
*Required*: Conditional\. You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NatGatewayId`  <a name="cfn-ec2-route-natgatewayid"></a>
The ID of a NAT gateway\. For example, `nat-0a12bc456789de0fg`\.  
*Required*: Conditional\. You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-route-networkinterfaceid"></a>
Allows the routing of network interface IDs\.  
*Required*: Conditional\. You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RouteTableId`  <a name="cfn-ec2-route-routetableid"></a>
The ID of the [route table](aws-resource-ec2-route-table.md) where the route will be added\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VpcPeeringConnectionId`  <a name="cfn-ec2-route-vpcpeeringconnectionid"></a>
The ID of a VPC peering connection\.  
*Required*: Conditional\. You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d454c11"></a>

### Ref<a name="w3ab2c21c10d454c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d454c13"></a>

The following example creates a route that is added to a gateway\.

### JSON<a name="aws-resource-ec2-route-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myRoute" : {
         "Type" : "AWS::EC2::Route",
         "DependsOn" : "GatewayToInternet",
         "Properties" : {
            "RouteTableId" : { "Ref" : "myRouteTable" },
            "DestinationCidrBlock" : "0.0.0.0/0",
            "GatewayId" : { "Ref" : "myInternetGateway" }
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-route-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myRoute:
    Type: AWS::EC2::Route
    DependsOn: GatewayToInternet
    Properties:
      RouteTableId:
        Ref: myRouteTable
      DestinationCidrBlock: 0.0.0.0/0
      GatewayId:
        Ref: myInternetGateway
```

## More Info<a name="w3ab2c21c10d454c15"></a>
+ [AWS::EC2::RouteTable](aws-resource-ec2-route-table.md)
+ [CreateRoute](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateRoute.html) in the *Amazon EC2 API Reference*
+ [Route Tables](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*