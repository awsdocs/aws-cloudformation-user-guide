# AWS::EC2::NetworkInsightsAnalysis Explanation<a name="aws-properties-ec2-networkinsightsanalysis-explanation"></a>

Describes an explanation code for an unreachable path\. For more information, see [Reachability Analyzer explanation codes](https://docs.aws.amazon.com/vpc/latest/reachability/explanation-codes.html)\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-explanation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-explanation-syntax.json"></a>

```
{
  "[Acl](#cfn-ec2-networkinsightsanalysis-explanation-acl)" : AnalysisComponent,
  "[AclRule](#cfn-ec2-networkinsightsanalysis-explanation-aclrule)" : AnalysisAclRule,
  "[Address](#cfn-ec2-networkinsightsanalysis-explanation-address)" : String,
  "[Addresses](#cfn-ec2-networkinsightsanalysis-explanation-addresses)" : [ String, ... ],
  "[AttachedTo](#cfn-ec2-networkinsightsanalysis-explanation-attachedto)" : AnalysisComponent,
  "[AvailabilityZones](#cfn-ec2-networkinsightsanalysis-explanation-availabilityzones)" : [ String, ... ],
  "[Cidrs](#cfn-ec2-networkinsightsanalysis-explanation-cidrs)" : [ String, ... ],
  "[ClassicLoadBalancerListener](#cfn-ec2-networkinsightsanalysis-explanation-classicloadbalancerlistener)" : AnalysisLoadBalancerListener,
  "[Component](#cfn-ec2-networkinsightsanalysis-explanation-component)" : AnalysisComponent,
  "[CustomerGateway](#cfn-ec2-networkinsightsanalysis-explanation-customergateway)" : AnalysisComponent,
  "[Destination](#cfn-ec2-networkinsightsanalysis-explanation-destination)" : AnalysisComponent,
  "[DestinationVpc](#cfn-ec2-networkinsightsanalysis-explanation-destinationvpc)" : AnalysisComponent,
  "[Direction](#cfn-ec2-networkinsightsanalysis-explanation-direction)" : String,
  "[ElasticLoadBalancerListener](#cfn-ec2-networkinsightsanalysis-explanation-elasticloadbalancerlistener)" : AnalysisComponent,
  "[ExplanationCode](#cfn-ec2-networkinsightsanalysis-explanation-explanationcode)" : String,
  "[IngressRouteTable](#cfn-ec2-networkinsightsanalysis-explanation-ingressroutetable)" : AnalysisComponent,
  "[InternetGateway](#cfn-ec2-networkinsightsanalysis-explanation-internetgateway)" : AnalysisComponent,
  "[LoadBalancerArn](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancerarn)" : String,
  "[LoadBalancerListenerPort](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancerlistenerport)" : Integer,
  "[LoadBalancerTarget](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancertarget)" : AnalysisLoadBalancerTarget,
  "[LoadBalancerTargetGroup](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetgroup)" : AnalysisComponent,
  "[LoadBalancerTargetGroups](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetgroups)" : [ AnalysisComponent, ... ],
  "[LoadBalancerTargetPort](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetport)" : Integer,
  "[MissingComponent](#cfn-ec2-networkinsightsanalysis-explanation-missingcomponent)" : String,
  "[NatGateway](#cfn-ec2-networkinsightsanalysis-explanation-natgateway)" : AnalysisComponent,
  "[NetworkInterface](#cfn-ec2-networkinsightsanalysis-explanation-networkinterface)" : AnalysisComponent,
  "[PacketField](#cfn-ec2-networkinsightsanalysis-explanation-packetfield)" : String,
  "[Port](#cfn-ec2-networkinsightsanalysis-explanation-port)" : Integer,
  "[PortRanges](#cfn-ec2-networkinsightsanalysis-explanation-portranges)" : [ PortRange, ... ],
  "[PrefixList](#cfn-ec2-networkinsightsanalysis-explanation-prefixlist)" : AnalysisComponent,
  "[Protocols](#cfn-ec2-networkinsightsanalysis-explanation-protocols)" : [ String, ... ],
  "[RouteTable](#cfn-ec2-networkinsightsanalysis-explanation-routetable)" : AnalysisComponent,
  "[RouteTableRoute](#cfn-ec2-networkinsightsanalysis-explanation-routetableroute)" : AnalysisRouteTableRoute,
  "[SecurityGroup](#cfn-ec2-networkinsightsanalysis-explanation-securitygroup)" : AnalysisComponent,
  "[SecurityGroupRule](#cfn-ec2-networkinsightsanalysis-explanation-securitygrouprule)" : AnalysisSecurityGroupRule,
  "[SecurityGroups](#cfn-ec2-networkinsightsanalysis-explanation-securitygroups)" : [ AnalysisComponent, ... ],
  "[SourceVpc](#cfn-ec2-networkinsightsanalysis-explanation-sourcevpc)" : AnalysisComponent,
  "[State](#cfn-ec2-networkinsightsanalysis-explanation-state)" : String,
  "[Subnet](#cfn-ec2-networkinsightsanalysis-explanation-subnet)" : AnalysisComponent,
  "[SubnetRouteTable](#cfn-ec2-networkinsightsanalysis-explanation-subnetroutetable)" : AnalysisComponent,
  "[Vpc](#cfn-ec2-networkinsightsanalysis-explanation-vpc)" : AnalysisComponent,
  "[vpcEndpoint](#cfn-ec2-networkinsightsanalysis-explanation-vpcendpoint)" : AnalysisComponent,
  "[VpcPeeringConnection](#cfn-ec2-networkinsightsanalysis-explanation-vpcpeeringconnection)" : AnalysisComponent,
  "[VpnConnection](#cfn-ec2-networkinsightsanalysis-explanation-vpnconnection)" : AnalysisComponent,
  "[VpnGateway](#cfn-ec2-networkinsightsanalysis-explanation-vpngateway)" : AnalysisComponent
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-explanation-syntax.yaml"></a>

```
  [Acl](#cfn-ec2-networkinsightsanalysis-explanation-acl): 
    AnalysisComponent
  [AclRule](#cfn-ec2-networkinsightsanalysis-explanation-aclrule): 
    AnalysisAclRule
  [Address](#cfn-ec2-networkinsightsanalysis-explanation-address): String
  [Addresses](#cfn-ec2-networkinsightsanalysis-explanation-addresses): 
    - String
  [AttachedTo](#cfn-ec2-networkinsightsanalysis-explanation-attachedto): 
    AnalysisComponent
  [AvailabilityZones](#cfn-ec2-networkinsightsanalysis-explanation-availabilityzones): 
    - String
  [Cidrs](#cfn-ec2-networkinsightsanalysis-explanation-cidrs): 
    - String
  [ClassicLoadBalancerListener](#cfn-ec2-networkinsightsanalysis-explanation-classicloadbalancerlistener): 
    AnalysisLoadBalancerListener
  [Component](#cfn-ec2-networkinsightsanalysis-explanation-component): 
    AnalysisComponent
  [CustomerGateway](#cfn-ec2-networkinsightsanalysis-explanation-customergateway): 
    AnalysisComponent
  [Destination](#cfn-ec2-networkinsightsanalysis-explanation-destination): 
    AnalysisComponent
  [DestinationVpc](#cfn-ec2-networkinsightsanalysis-explanation-destinationvpc): 
    AnalysisComponent
  [Direction](#cfn-ec2-networkinsightsanalysis-explanation-direction): String
  [ElasticLoadBalancerListener](#cfn-ec2-networkinsightsanalysis-explanation-elasticloadbalancerlistener): 
    AnalysisComponent
  [ExplanationCode](#cfn-ec2-networkinsightsanalysis-explanation-explanationcode): String
  [IngressRouteTable](#cfn-ec2-networkinsightsanalysis-explanation-ingressroutetable): 
    AnalysisComponent
  [InternetGateway](#cfn-ec2-networkinsightsanalysis-explanation-internetgateway): 
    AnalysisComponent
  [LoadBalancerArn](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancerarn): String
  [LoadBalancerListenerPort](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancerlistenerport): Integer
  [LoadBalancerTarget](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancertarget): 
    AnalysisLoadBalancerTarget
  [LoadBalancerTargetGroup](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetgroup): 
    AnalysisComponent
  [LoadBalancerTargetGroups](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetgroups): 
    - AnalysisComponent
  [LoadBalancerTargetPort](#cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetport): Integer
  [MissingComponent](#cfn-ec2-networkinsightsanalysis-explanation-missingcomponent): String
  [NatGateway](#cfn-ec2-networkinsightsanalysis-explanation-natgateway): 
    AnalysisComponent
  [NetworkInterface](#cfn-ec2-networkinsightsanalysis-explanation-networkinterface): 
    AnalysisComponent
  [PacketField](#cfn-ec2-networkinsightsanalysis-explanation-packetfield): String
  [Port](#cfn-ec2-networkinsightsanalysis-explanation-port): Integer
  [PortRanges](#cfn-ec2-networkinsightsanalysis-explanation-portranges): 
    - PortRange
  [PrefixList](#cfn-ec2-networkinsightsanalysis-explanation-prefixlist): 
    AnalysisComponent
  [Protocols](#cfn-ec2-networkinsightsanalysis-explanation-protocols): 
    - String
  [RouteTable](#cfn-ec2-networkinsightsanalysis-explanation-routetable): 
    AnalysisComponent
  [RouteTableRoute](#cfn-ec2-networkinsightsanalysis-explanation-routetableroute): 
    AnalysisRouteTableRoute
  [SecurityGroup](#cfn-ec2-networkinsightsanalysis-explanation-securitygroup): 
    AnalysisComponent
  [SecurityGroupRule](#cfn-ec2-networkinsightsanalysis-explanation-securitygrouprule): 
    AnalysisSecurityGroupRule
  [SecurityGroups](#cfn-ec2-networkinsightsanalysis-explanation-securitygroups): 
    - AnalysisComponent
  [SourceVpc](#cfn-ec2-networkinsightsanalysis-explanation-sourcevpc): 
    AnalysisComponent
  [State](#cfn-ec2-networkinsightsanalysis-explanation-state): String
  [Subnet](#cfn-ec2-networkinsightsanalysis-explanation-subnet): 
    AnalysisComponent
  [SubnetRouteTable](#cfn-ec2-networkinsightsanalysis-explanation-subnetroutetable): 
    AnalysisComponent
  [Vpc](#cfn-ec2-networkinsightsanalysis-explanation-vpc): 
    AnalysisComponent
  [vpcEndpoint](#cfn-ec2-networkinsightsanalysis-explanation-vpcendpoint): 
    AnalysisComponent
  [VpcPeeringConnection](#cfn-ec2-networkinsightsanalysis-explanation-vpcpeeringconnection): 
    AnalysisComponent
  [VpnConnection](#cfn-ec2-networkinsightsanalysis-explanation-vpnconnection): 
    AnalysisComponent
  [VpnGateway](#cfn-ec2-networkinsightsanalysis-explanation-vpngateway): 
    AnalysisComponent
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-explanation-properties"></a>

`Acl`  <a name="cfn-ec2-networkinsightsanalysis-explanation-acl"></a>
The network ACL\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AclRule`  <a name="cfn-ec2-networkinsightsanalysis-explanation-aclrule"></a>
The network ACL rule\.  
*Required*: No  
*Type*: [AnalysisAclRule](aws-properties-ec2-networkinsightsanalysis-analysisaclrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Address`  <a name="cfn-ec2-networkinsightsanalysis-explanation-address"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Addresses`  <a name="cfn-ec2-networkinsightsanalysis-explanation-addresses"></a>
The IPv4 addresses, in CIDR notation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AttachedTo`  <a name="cfn-ec2-networkinsightsanalysis-explanation-attachedto"></a>
The resource to which the component is attached\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZones`  <a name="cfn-ec2-networkinsightsanalysis-explanation-availabilityzones"></a>
The Availability Zones\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cidrs`  <a name="cfn-ec2-networkinsightsanalysis-explanation-cidrs"></a>
The CIDR ranges\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClassicLoadBalancerListener`  <a name="cfn-ec2-networkinsightsanalysis-explanation-classicloadbalancerlistener"></a>
The listener for a Classic Load Balancer\.  
*Required*: No  
*Type*: [AnalysisLoadBalancerListener](aws-properties-ec2-networkinsightsanalysis-analysisloadbalancerlistener.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Component`  <a name="cfn-ec2-networkinsightsanalysis-explanation-component"></a>
The component\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomerGateway`  <a name="cfn-ec2-networkinsightsanalysis-explanation-customergateway"></a>
The customer gateway\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-ec2-networkinsightsanalysis-explanation-destination"></a>
The destination\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationVpc`  <a name="cfn-ec2-networkinsightsanalysis-explanation-destinationvpc"></a>
The destination VPC\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Direction`  <a name="cfn-ec2-networkinsightsanalysis-explanation-direction"></a>
The direction\. The following are possible values:  
+ egress
+ ingress
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElasticLoadBalancerListener`  <a name="cfn-ec2-networkinsightsanalysis-explanation-elasticloadbalancerlistener"></a>
The load balancer listener\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExplanationCode`  <a name="cfn-ec2-networkinsightsanalysis-explanation-explanationcode"></a>
The explanation code\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngressRouteTable`  <a name="cfn-ec2-networkinsightsanalysis-explanation-ingressroutetable"></a>
The route table\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InternetGateway`  <a name="cfn-ec2-networkinsightsanalysis-explanation-internetgateway"></a>
The internet gateway\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerArn`  <a name="cfn-ec2-networkinsightsanalysis-explanation-loadbalancerarn"></a>
The Amazon Resource Name \(ARN\) of the load balancer\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1283`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerListenerPort`  <a name="cfn-ec2-networkinsightsanalysis-explanation-loadbalancerlistenerport"></a>
The listener port of the load balancer\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerTarget`  <a name="cfn-ec2-networkinsightsanalysis-explanation-loadbalancertarget"></a>
The target\.  
*Required*: No  
*Type*: [AnalysisLoadBalancerTarget](aws-properties-ec2-networkinsightsanalysis-analysisloadbalancertarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerTargetGroup`  <a name="cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetgroup"></a>
The target group\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerTargetGroups`  <a name="cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetgroups"></a>
The target groups\.  
*Required*: No  
*Type*: List of [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerTargetPort`  <a name="cfn-ec2-networkinsightsanalysis-explanation-loadbalancertargetport"></a>
The target port\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MissingComponent`  <a name="cfn-ec2-networkinsightsanalysis-explanation-missingcomponent"></a>
The missing component\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NatGateway`  <a name="cfn-ec2-networkinsightsanalysis-explanation-natgateway"></a>
The NAT gateway\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterface`  <a name="cfn-ec2-networkinsightsanalysis-explanation-networkinterface"></a>
The network interface\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PacketField`  <a name="cfn-ec2-networkinsightsanalysis-explanation-packetfield"></a>
The packet field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-ec2-networkinsightsanalysis-explanation-port"></a>
The port\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortRanges`  <a name="cfn-ec2-networkinsightsanalysis-explanation-portranges"></a>
The port ranges\.  
*Required*: No  
*Type*: List of [PortRange](aws-properties-ec2-networkinsightsanalysis-portrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrefixList`  <a name="cfn-ec2-networkinsightsanalysis-explanation-prefixlist"></a>
The prefix list\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocols`  <a name="cfn-ec2-networkinsightsanalysis-explanation-protocols"></a>
The protocols\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteTable`  <a name="cfn-ec2-networkinsightsanalysis-explanation-routetable"></a>
The route table\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteTableRoute`  <a name="cfn-ec2-networkinsightsanalysis-explanation-routetableroute"></a>
The route table route\.  
*Required*: No  
*Type*: [AnalysisRouteTableRoute](aws-properties-ec2-networkinsightsanalysis-analysisroutetableroute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroup`  <a name="cfn-ec2-networkinsightsanalysis-explanation-securitygroup"></a>
The security group\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupRule`  <a name="cfn-ec2-networkinsightsanalysis-explanation-securitygrouprule"></a>
The security group rule\.  
*Required*: No  
*Type*: [AnalysisSecurityGroupRule](aws-properties-ec2-networkinsightsanalysis-analysissecuritygrouprule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroups`  <a name="cfn-ec2-networkinsightsanalysis-explanation-securitygroups"></a>
The security groups\.  
*Required*: No  
*Type*: List of [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceVpc`  <a name="cfn-ec2-networkinsightsanalysis-explanation-sourcevpc"></a>
The source VPC\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-ec2-networkinsightsanalysis-explanation-state"></a>
The state\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subnet`  <a name="cfn-ec2-networkinsightsanalysis-explanation-subnet"></a>
The subnet\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetRouteTable`  <a name="cfn-ec2-networkinsightsanalysis-explanation-subnetroutetable"></a>
The route table for the subnet\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Vpc`  <a name="cfn-ec2-networkinsightsanalysis-explanation-vpc"></a>
The component VPC\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`vpcEndpoint`  <a name="cfn-ec2-networkinsightsanalysis-explanation-vpcendpoint"></a>
The VPC endpoint\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcPeeringConnection`  <a name="cfn-ec2-networkinsightsanalysis-explanation-vpcpeeringconnection"></a>
The VPC peering connection\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpnConnection`  <a name="cfn-ec2-networkinsightsanalysis-explanation-vpnconnection"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpnGateway`  <a name="cfn-ec2-networkinsightsanalysis-explanation-vpngateway"></a>
The VPN gateway\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)