# AWS::EC2::Route<a name="aws-resource-ec2-route"></a>

Specifies a route in a route table within a VPC\.

You must specify either `DestinationCidrBlock` or `DestinationIpv6CidrBlock`, plus the ID of one of the target resources\.

If you create a route that references a transit gateway in the same template where you create the transit gateway, you must declare a dependency on the transit gateway attachment\. The route table cannot use the transit gateway until it has successfully attached to the VPC\. Add a [ DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) in the `AWS::EC2::Route` resource to explicitly declare a dependency on the `AWS::EC2::TransitGatewayAttachment` resource\.

## Syntax<a name="aws-resource-ec2-route-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-route-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::Route",
  "Properties" : {
      "[CarrierGatewayId](#cfn-ec2-route-carriergatewayid)" : String,
      "[DestinationCidrBlock](#cfn-ec2-route-destinationcidrblock)" : String,
      "[DestinationIpv6CidrBlock](#cfn-ec2-route-destinationipv6cidrblock)" : String,
      "[EgressOnlyInternetGatewayId](#cfn-ec2-route-egressonlyinternetgatewayid)" : String,
      "[GatewayId](#cfn-ec2-route-gatewayid)" : String,
      "[InstanceId](#cfn-ec2-route-instanceid)" : String,
      "[LocalGatewayId](#cfn-ec2-route-localgatewayid)" : String,
      "[NatGatewayId](#cfn-ec2-route-natgatewayid)" : String,
      "[NetworkInterfaceId](#cfn-ec2-route-networkinterfaceid)" : String,
      "[RouteTableId](#cfn-ec2-route-routetableid)" : String,
      "[TransitGatewayId](#cfn-ec2-route-transitgatewayid)" : String,
      "[VpcEndpointId](#cfn-ec2-route-vpcendpointid)" : String,
      "[VpcPeeringConnectionId](#cfn-ec2-route-vpcpeeringconnectionid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-route-syntax.yaml"></a>

```
Type: AWS::EC2::Route
Properties: 
  [CarrierGatewayId](#cfn-ec2-route-carriergatewayid): String
  [DestinationCidrBlock](#cfn-ec2-route-destinationcidrblock): String
  [DestinationIpv6CidrBlock](#cfn-ec2-route-destinationipv6cidrblock): String
  [EgressOnlyInternetGatewayId](#cfn-ec2-route-egressonlyinternetgatewayid): String
  [GatewayId](#cfn-ec2-route-gatewayid): String
  [InstanceId](#cfn-ec2-route-instanceid): String
  [LocalGatewayId](#cfn-ec2-route-localgatewayid): String
  [NatGatewayId](#cfn-ec2-route-natgatewayid): String
  [NetworkInterfaceId](#cfn-ec2-route-networkinterfaceid): String
  [RouteTableId](#cfn-ec2-route-routetableid): String
  [TransitGatewayId](#cfn-ec2-route-transitgatewayid): String
  [VpcEndpointId](#cfn-ec2-route-vpcendpointid): String
  [VpcPeeringConnectionId](#cfn-ec2-route-vpcpeeringconnectionid): String
```

## Properties<a name="aws-resource-ec2-route-properties"></a>

`CarrierGatewayId`  <a name="cfn-ec2-route-carriergatewayid"></a>
The ID of the carrier gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationCidrBlock`  <a name="cfn-ec2-route-destinationcidrblock"></a>
The IPv4 CIDR block used for the destination match\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationIpv6CidrBlock`  <a name="cfn-ec2-route-destinationipv6cidrblock"></a>
The IPv6 CIDR block used for the destination match\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EgressOnlyInternetGatewayId`  <a name="cfn-ec2-route-egressonlyinternetgatewayid"></a>
The ID of the egress\-only internet gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GatewayId`  <a name="cfn-ec2-route-gatewayid"></a>
The ID of an internet gateway or virtual private gateway attached to your VPC\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceId`  <a name="cfn-ec2-route-instanceid"></a>
The ID of a NAT instance in your VPC\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocalGatewayId`  <a name="cfn-ec2-route-localgatewayid"></a>
The ID of the local gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NatGatewayId`  <a name="cfn-ec2-route-natgatewayid"></a>
The ID of a NAT gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-route-networkinterfaceid"></a>
The ID of the network interface\.  
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

`VpcEndpointId`  <a name="cfn-ec2-route-vpcendpointid"></a>
The ID of a VPC endpoint\. Supported for Gateway Load Balancer endpoints only\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcPeeringConnectionId`  <a name="cfn-ec2-route-vpcpeeringconnectionid"></a>
The ID of a VPC peering connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-route-return-values"></a>

### Ref<a name="aws-resource-ec2-route-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the route\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-route--examples"></a>



### Create a route to a gateway<a name="aws-resource-ec2-route--examples--Create_a_route_to_a_gateway"></a>

The following example adds a route that is added to an internet gateway\.

#### JSON<a name="aws-resource-ec2-route--examples--Create_a_route_to_a_gateway--json"></a>

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

#### YAML<a name="aws-resource-ec2-route--examples--Create_a_route_to_a_gateway--yaml"></a>

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

### Create a route to a carrier gateway<a name="aws-resource-ec2-route--examples--Create_a_route_to_a_carrier_gateway"></a>

The following example creates a route to a carrier gateway\.

#### JSON<a name="aws-resource-ec2-route--examples--Create_a_route_to_a_carrier_gateway--json"></a>

```
"myCarrierRoute" : {
   "Type" : "AWS::EC2::Route",
   "DependsOn" : "GatewayToInternetAndCarrierNetwork",
   "Properties" : {
      "RouteTableId" : { "Ref" : "myRouteTable" },
      "DestinationCidrBlock" : "0.0.0.0/0",
      "GatewayId" : { "Ref" : "myCarrierGateway" }
   }
}
```

#### YAML<a name="aws-resource-ec2-route--examples--Create_a_route_to_a_carrier_gateway--yaml"></a>

```
 myCarrierRoute:
    Type: AWS::EC2::Route
    DependsOn: GatewayToInternetAndCarrierNetwork
    Properties:
       RouteTableId:
         Ref: myRouteTable
       DestinationCidrBlock: 0.0.0.0/0
       GatewayId:
         Ref: myCarrierGateway
```

## See also<a name="aws-resource-ec2-route--seealso"></a>
+  [CreateRoute](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateRoute.html) in the *Amazon EC2 API Reference*
+  [Route tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*

