# AWS::EC2::NetworkInsightsAnalysis PathComponent<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent"></a>

Describes a path component\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent-syntax.json"></a>

```
{
  "[AclRule](#cfn-ec2-networkinsightsanalysis-pathcomponent-aclrule)" : AnalysisAclRule,
  "[AdditionalDetails](#cfn-ec2-networkinsightsanalysis-pathcomponent-additionaldetails)" : [ AdditionalDetail, ... ],
  "[Component](#cfn-ec2-networkinsightsanalysis-pathcomponent-component)" : AnalysisComponent,
  "[DestinationVpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-destinationvpc)" : AnalysisComponent,
  "[ElasticLoadBalancerListener](#cfn-ec2-networkinsightsanalysis-pathcomponent-elasticloadbalancerlistener)" : AnalysisComponent,
  "[Explanations](#cfn-ec2-networkinsightsanalysis-pathcomponent-explanations)" : [ Explanation, ... ],
  "[InboundHeader](#cfn-ec2-networkinsightsanalysis-pathcomponent-inboundheader)" : AnalysisPacketHeader,
  "[OutboundHeader](#cfn-ec2-networkinsightsanalysis-pathcomponent-outboundheader)" : AnalysisPacketHeader,
  "[RouteTableRoute](#cfn-ec2-networkinsightsanalysis-pathcomponent-routetableroute)" : AnalysisRouteTableRoute,
  "[SecurityGroupRule](#cfn-ec2-networkinsightsanalysis-pathcomponent-securitygrouprule)" : AnalysisSecurityGroupRule,
  "[SequenceNumber](#cfn-ec2-networkinsightsanalysis-pathcomponent-sequencenumber)" : Integer,
  "[ServiceName](#cfn-ec2-networkinsightsanalysis-pathcomponent-servicename)" : String,
  "[SourceVpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-sourcevpc)" : AnalysisComponent,
  "[Subnet](#cfn-ec2-networkinsightsanalysis-pathcomponent-subnet)" : AnalysisComponent,
  "[TransitGateway](#cfn-ec2-networkinsightsanalysis-pathcomponent-transitgateway)" : AnalysisComponent,
  "[TransitGatewayRouteTableRoute](#cfn-ec2-networkinsightsanalysis-pathcomponent-transitgatewayroutetableroute)" : TransitGatewayRouteTableRoute,
  "[Vpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-vpc)" : AnalysisComponent
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent-syntax.yaml"></a>

```
  [AclRule](#cfn-ec2-networkinsightsanalysis-pathcomponent-aclrule): 
    AnalysisAclRule
  [AdditionalDetails](#cfn-ec2-networkinsightsanalysis-pathcomponent-additionaldetails): 
    - AdditionalDetail
  [Component](#cfn-ec2-networkinsightsanalysis-pathcomponent-component): 
    AnalysisComponent
  [DestinationVpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-destinationvpc): 
    AnalysisComponent
  [ElasticLoadBalancerListener](#cfn-ec2-networkinsightsanalysis-pathcomponent-elasticloadbalancerlistener): 
    AnalysisComponent
  [Explanations](#cfn-ec2-networkinsightsanalysis-pathcomponent-explanations): 
    - Explanation
  [InboundHeader](#cfn-ec2-networkinsightsanalysis-pathcomponent-inboundheader): 
    AnalysisPacketHeader
  [OutboundHeader](#cfn-ec2-networkinsightsanalysis-pathcomponent-outboundheader): 
    AnalysisPacketHeader
  [RouteTableRoute](#cfn-ec2-networkinsightsanalysis-pathcomponent-routetableroute): 
    AnalysisRouteTableRoute
  [SecurityGroupRule](#cfn-ec2-networkinsightsanalysis-pathcomponent-securitygrouprule): 
    AnalysisSecurityGroupRule
  [SequenceNumber](#cfn-ec2-networkinsightsanalysis-pathcomponent-sequencenumber): Integer
  [ServiceName](#cfn-ec2-networkinsightsanalysis-pathcomponent-servicename): String
  [SourceVpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-sourcevpc): 
    AnalysisComponent
  [Subnet](#cfn-ec2-networkinsightsanalysis-pathcomponent-subnet): 
    AnalysisComponent
  [TransitGateway](#cfn-ec2-networkinsightsanalysis-pathcomponent-transitgateway): 
    AnalysisComponent
  [TransitGatewayRouteTableRoute](#cfn-ec2-networkinsightsanalysis-pathcomponent-transitgatewayroutetableroute): 
    TransitGatewayRouteTableRoute
  [Vpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-vpc): 
    AnalysisComponent
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent-properties"></a>

`AclRule`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-aclrule"></a>
The network ACL rule\.  
*Required*: No  
*Type*: [AnalysisAclRule](aws-properties-ec2-networkinsightsanalysis-analysisaclrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdditionalDetails`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-additionaldetails"></a>
The additional details\.  
*Required*: No  
*Type*: List of [AdditionalDetail](aws-properties-ec2-networkinsightsanalysis-additionaldetail.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Component`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-component"></a>
The component\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationVpc`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-destinationvpc"></a>
The destination VPC\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticLoadBalancerListener`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-elasticloadbalancerlistener"></a>
The load balancer listener\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Explanations`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-explanations"></a>
The explanation codes\.  
*Required*: No  
*Type*: List of [Explanation](aws-properties-ec2-networkinsightsanalysis-explanation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InboundHeader`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-inboundheader"></a>
The inbound header\.  
*Required*: No  
*Type*: [AnalysisPacketHeader](aws-properties-ec2-networkinsightsanalysis-analysispacketheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutboundHeader`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-outboundheader"></a>
The outbound header\.  
*Required*: No  
*Type*: [AnalysisPacketHeader](aws-properties-ec2-networkinsightsanalysis-analysispacketheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteTableRoute`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-routetableroute"></a>
The route table route\.  
*Required*: No  
*Type*: [AnalysisRouteTableRoute](aws-properties-ec2-networkinsightsanalysis-analysisroutetableroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupRule`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-securitygrouprule"></a>
The security group rule\.  
*Required*: No  
*Type*: [AnalysisSecurityGroupRule](aws-properties-ec2-networkinsightsanalysis-analysissecuritygrouprule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SequenceNumber`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-sequencenumber"></a>
The sequence number\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-servicename"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceVpc`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-sourcevpc"></a>
The source VPC\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subnet`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-subnet"></a>
The subnet\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGateway`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-transitgateway"></a>
The transit gateway\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitGatewayRouteTableRoute`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-transitgatewayroutetableroute"></a>
The route in a transit gateway route table\.  
*Required*: No  
*Type*: [TransitGatewayRouteTableRoute](aws-properties-ec2-networkinsightsanalysis-transitgatewayroutetableroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Vpc`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-vpc"></a>
The component VPC\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)