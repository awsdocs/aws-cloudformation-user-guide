# AWS::EC2::Route<a name="aws-resource-ec2-route"></a>

Specifies a route in a route table within a VPC\.

You must specify one of the following targets: internet gateway or virtual private gateway, NAT instance, NAT gateway, VPC peering connection, network interface, or egress\-only internet gateway\.

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
      "[TransitGatewayId](#cfn-ec2-route-transitgatewayid)" : String,
      "[VpcPeeringConnectionId](#cfn-ec2-route-vpcpeeringconnectionid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-route-syntax.yaml"></a>

```
Type: AWS::EC2::Route
Properties: 
  [DestinationCidrBlock](#cfn-ec2-route-destinationcidrblock): String
  [DestinationIpv6CidrBlock](#cfn-ec2-route-destinationipv6cidrblock): String
  [EgressOnlyInternetGatewayId](#cfn-ec2-route-egressonlyinternetgatewayid): String
  [GatewayId](#cfn-ec2-route-gatewayid): String
  [InstanceId](#cfn-ec2-route-instanceid): String
  [NatGatewayId](#cfn-ec2-route-natgatewayid): String
  [NetworkInterfaceId](#cfn-ec2-route-networkinterfaceid): String
  [RouteTableId](#cfn-ec2-route-routetableid): String
  [TransitGatewayId](#cfn-ec2-route-transitgatewayid): String
  [VpcPeeringConnectionId](#cfn-ec2-route-vpcpeeringconnectionid): String
```

## Properties<a name="aws-resource-ec2-route-properties"></a>

`DestinationCidrBlock`  <a name="cfn-ec2-route-destinationcidrblock"></a>
The IPv4 CIDR block used for the destination match\.  
You must specify the `DestinationCidrBlock` or `DestinationIpv6CidrBlock` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationIpv6CidrBlock`  <a name="cfn-ec2-route-destinationipv6cidrblock"></a>
The IPv6 CIDR block used for the destination match\.  
You must specify the `DestinationCidrBlock` or `DestinationIpv6CidrBlock` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EgressOnlyInternetGatewayId`  <a name="cfn-ec2-route-egressonlyinternetgatewayid"></a>
The ID of the egress\-only internet gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GatewayId`  <a name="cfn-ec2-route-gatewayid"></a>
The ID of a gateway attached to your VPC\.  
 You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceId`  <a name="cfn-ec2-route-instanceid"></a>
The ID of a NAT instance in your VPC\.  
You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NatGatewayId`  <a name="cfn-ec2-route-natgatewayid"></a>
The ID of a NAT gateway\.  
You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-route-networkinterfaceid"></a>
The ID of the network interface\.  
You must specify only one of the following properties: `EgressOnlyInternetGatewayId`, `GatewayId`, `InstanceId`, `NatGatewayId`, `NetworkInterfaceId`, or `VpcPeeringConnectionId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteTableId`  <a name="cfn-ec2-route-routetableid"></a>
The ID of the route table\. The routing table must be associated with the same VPC that the virtual private gateway is attached to\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitGatewayId`  <a name="cfn-ec2-route-transitgatewayid"></a>
The ID of a transit gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcPeeringConnectionId`  <a name="cfn-ec2-route-vpcpeeringconnectionid"></a>
The ID of a VPC peering connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-ec2-route-return-values"></a>

### Ref<a name="aws-resource-ec2-route-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the route\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-route--examples"></a>

### Add a Route<a name="aws-resource-ec2-route--examples--Add_a_Route"></a>

The following example adds a route that is added to a gateway\.

#### JSON<a name="aws-resource-ec2-route--examples--Add_a_Route--json"></a>

```
"myRoute" : {
   "Type" : "AWS::EC2::Route",
   "DependsOn" : "GatewayToInternet",
   "Properties" : {
      "RouteTableId" : { "Ref" : "myRouteTable" },
      "DestinationCidrBlock" : "0.0.0.0/0",
      "GatewayId" : { "Ref" : "myInternetGateway" }
   }
}
```

#### YAML<a name="aws-resource-ec2-route--examples--Add_a_Route--yaml"></a>

```
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

## See Also<a name="aws-resource-ec2-route--seealso"></a>
+  [CreateRoute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateRoute.html) in the *Amazon EC2 API Reference*
+  [Route Tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*