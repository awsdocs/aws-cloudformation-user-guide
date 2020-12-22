# AWS::EC2::NetworkInsightsAnalysis PathComponent<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent"></a>

Describes a path component\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent-syntax.json"></a>

```
{
  "[AclRule](#cfn-ec2-networkinsightsanalysis-pathcomponent-aclrule)" : AnalysisAclRule,
  "[Component](#cfn-ec2-networkinsightsanalysis-pathcomponent-component)" : AnalysisComponent,
  "[DestinationVpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-destinationvpc)" : AnalysisComponent,
  "[InboundHeader](#cfn-ec2-networkinsightsanalysis-pathcomponent-inboundheader)" : AnalysisPacketHeader,
  "[OutboundHeader](#cfn-ec2-networkinsightsanalysis-pathcomponent-outboundheader)" : AnalysisPacketHeader,
  "[RouteTableRoute](#cfn-ec2-networkinsightsanalysis-pathcomponent-routetableroute)" : AnalysisRouteTableRoute,
  "[SecurityGroupRule](#cfn-ec2-networkinsightsanalysis-pathcomponent-securitygrouprule)" : AnalysisSecurityGroupRule,
  "[SequenceNumber](#cfn-ec2-networkinsightsanalysis-pathcomponent-sequencenumber)" : Integer,
  "[SourceVpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-sourcevpc)" : AnalysisComponent,
  "[Subnet](#cfn-ec2-networkinsightsanalysis-pathcomponent-subnet)" : AnalysisComponent,
  "[Vpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-vpc)" : AnalysisComponent
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent-syntax.yaml"></a>

```
  [AclRule](#cfn-ec2-networkinsightsanalysis-pathcomponent-aclrule): 
    AnalysisAclRule
  [Component](#cfn-ec2-networkinsightsanalysis-pathcomponent-component): 
    AnalysisComponent
  [DestinationVpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-destinationvpc): 
    AnalysisComponent
  [InboundHeader](#cfn-ec2-networkinsightsanalysis-pathcomponent-inboundheader): 
    AnalysisPacketHeader
  [OutboundHeader](#cfn-ec2-networkinsightsanalysis-pathcomponent-outboundheader): 
    AnalysisPacketHeader
  [RouteTableRoute](#cfn-ec2-networkinsightsanalysis-pathcomponent-routetableroute): 
    AnalysisRouteTableRoute
  [SecurityGroupRule](#cfn-ec2-networkinsightsanalysis-pathcomponent-securitygrouprule): 
    AnalysisSecurityGroupRule
  [SequenceNumber](#cfn-ec2-networkinsightsanalysis-pathcomponent-sequencenumber): Integer
  [SourceVpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-sourcevpc): 
    AnalysisComponent
  [Subnet](#cfn-ec2-networkinsightsanalysis-pathcomponent-subnet): 
    AnalysisComponent
  [Vpc](#cfn-ec2-networkinsightsanalysis-pathcomponent-vpc): 
    AnalysisComponent
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-pathcomponent-properties"></a>

`AclRule`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-aclrule"></a>
The network ACL rule\.  
*Required*: No  
*Type*: [AnalysisAclRule](aws-properties-ec2-networkinsightsanalysis-analysisaclrule.md)  
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

`Vpc`  <a name="cfn-ec2-networkinsightsanalysis-pathcomponent-vpc"></a>
The component VPC\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)