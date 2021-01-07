# AWS::EC2::NetworkInsightsAnalysis AnalysisRouteTableRoute<a name="aws-properties-ec2-networkinsightsanalysis-analysisroutetableroute"></a>

Describes a route table route\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-analysisroutetableroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-analysisroutetableroute-syntax.json"></a>

```
{
  "[destinationCidr](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-destinationcidr)" : String,
  "[destinationPrefixListId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-destinationprefixlistid)" : String,
  "[egressOnlyInternetGatewayId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-egressonlyinternetgatewayid)" : String,
  "[gatewayId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-gatewayid)" : String,
  "[instanceId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-instanceid)" : String,
  "[NatGatewayId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-natgatewayid)" : String,
  "[NetworkInterfaceId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-networkinterfaceid)" : String,
  "[Origin](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-origin)" : String,
  "[TransitGatewayId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-transitgatewayid)" : String,
  "[VpcPeeringConnectionId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-vpcpeeringconnectionid)" : String
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-analysisroutetableroute-syntax.yaml"></a>

```
  [destinationCidr](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-destinationcidr): String
  [destinationPrefixListId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-destinationprefixlistid): String
  [egressOnlyInternetGatewayId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-egressonlyinternetgatewayid): String
  [gatewayId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-gatewayid): String
  [instanceId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-instanceid): String
  [NatGatewayId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-natgatewayid): String
  [NetworkInterfaceId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-networkinterfaceid): String
  [Origin](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-origin): String
  [TransitGatewayId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-transitgatewayid): String
  [VpcPeeringConnectionId](#cfn-ec2-networkinsightsanalysis-analysisroutetableroute-vpcpeeringconnectionid): String
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-analysisroutetableroute-properties"></a>

`destinationCidr`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-destinationcidr"></a>
The destination IPv4 address, in CIDR notation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`destinationPrefixListId`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-destinationprefixlistid"></a>
The prefix of the AWS service\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`egressOnlyInternetGatewayId`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-egressonlyinternetgatewayid"></a>
The ID of an egress\-only internet gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`gatewayId`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-gatewayid"></a>
The ID of the gateway, such as an internet gateway or virtual private gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`instanceId`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-instanceid"></a>
The ID of the instance, such as a NAT instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NatGatewayId`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-natgatewayid"></a>
The ID of a NAT gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-networkinterfaceid"></a>
The ID of a network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Origin`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-origin"></a>
Describes how the route was created\. The following are possible values:  
+  `CreateRouteTable` \- The route was automatically created when the route table was created\.
+  `CreateRoute` \- The route was manually added to the route table\.
+  `EnableVgwRoutePropagation` \- The route was propagated by route propagation\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGatewayId`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-transitgatewayid"></a>
The ID of a transit gateway\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcPeeringConnectionId`  <a name="cfn-ec2-networkinsightsanalysis-analysisroutetableroute-vpcpeeringconnectionid"></a>
The ID of a VPC peering connection\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)