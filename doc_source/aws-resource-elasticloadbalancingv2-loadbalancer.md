# AWS::ElasticLoadBalancingV2::LoadBalancer<a name="aws-resource-elasticloadbalancingv2-loadbalancer"></a>

Specifies an Application Load Balancer or a Network Load Balancer\.

## Syntax<a name="aws-resource-elasticloadbalancingv2-loadbalancer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-loadbalancer-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::LoadBalancer",
  "Properties" : {
      "[IpAddressType](#cfn-elasticloadbalancingv2-loadbalancer-ipaddresstype)" : String,
      "[LoadBalancerAttributes](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes)" : [ LoadBalancerAttribute, ... ],
      "[Name](#cfn-elasticloadbalancingv2-loadbalancer-name)" : String,
      "[Scheme](#cfn-elasticloadbalancingv2-loadbalancer-scheme)" : String,
      "[SecurityGroups](#cfn-elasticloadbalancingv2-loadbalancer-securitygroups)" : [ String, ... ],
      "[SubnetMappings](#cfn-elasticloadbalancingv2-loadbalancer-subnetmappings)" : [ SubnetMapping, ... ],
      "[Subnets](#cfn-elasticloadbalancingv2-loadbalancer-subnets)" : [ String, ... ],
      "[Tags](#cfn-elasticloadbalancingv2-loadbalancer-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-elasticloadbalancingv2-loadbalancer-type)" : String
    }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-loadbalancer-syntax.yaml"></a>

```
Type: AWS::ElasticLoadBalancingV2::LoadBalancer
Properties: 
  [IpAddressType](#cfn-elasticloadbalancingv2-loadbalancer-ipaddresstype): String
  [LoadBalancerAttributes](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes): 
    - LoadBalancerAttribute
  [Name](#cfn-elasticloadbalancingv2-loadbalancer-name): String
  [Scheme](#cfn-elasticloadbalancingv2-loadbalancer-scheme): String
  [SecurityGroups](#cfn-elasticloadbalancingv2-loadbalancer-securitygroups): 
    - String
  [SubnetMappings](#cfn-elasticloadbalancingv2-loadbalancer-subnetmappings): 
    - SubnetMapping
  [Subnets](#cfn-elasticloadbalancingv2-loadbalancer-subnets): 
    - String
  [Tags](#cfn-elasticloadbalancingv2-loadbalancer-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-elasticloadbalancingv2-loadbalancer-type): String
```

## Properties<a name="aws-resource-elasticloadbalancingv2-loadbalancer-properties"></a>

`IpAddressType`  <a name="cfn-elasticloadbalancingv2-loadbalancer-ipaddresstype"></a>
The IP address type\. The possible values are `ipv4` \(for IPv4 addresses\) and `dualstack` \(for IPv4 and IPv6 addresses\)\. Internal load balancers must use `ipv4`\. You can’t specify `dualstack` for a load balancer with a UDP or TCP\_UDP listener\.  
*Required*: No  
*Type*: String  
*Allowed values*: `dualstack | ipv4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerAttributes`  <a name="cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes"></a>
The load balancer attributes\.  
*Required*: No  
*Type*: List of [LoadBalancerAttribute](aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-elasticloadbalancingv2-loadbalancer-name"></a>
The name of the load balancer\. This name must be unique per region per account, can have a maximum of 32 characters, must contain only alphanumeric characters or hyphens, must not begin or end with a hyphen, and must not begin with "internal\-"\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID for the load balancer\. If you specify a name, you cannot perform updates that require replacement of this resource, but you can perform other updates\. To replace the resource, specify a new name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Scheme`  <a name="cfn-elasticloadbalancingv2-loadbalancer-scheme"></a>
The nodes of an Internet\-facing load balancer have public IP addresses\. The DNS name of an Internet\-facing load balancer is publicly resolvable to the public IP addresses of the nodes\. Therefore, Internet\-facing load balancers can route requests from clients over the internet\.  
The nodes of an internal load balancer have only private IP addresses\. The DNS name of an internal load balancer is publicly resolvable to the private IP addresses of the nodes\. Therefore, internal load balancers can route requests only from clients with access to the VPC for the load balancer\.  
The default is an Internet\-facing load balancer\.  
You cannot specify a scheme for a Gateway Load Balancer\.  
*Required*: No  
*Type*: String  
*Allowed values*: `internal | internet-facing`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-elasticloadbalancingv2-loadbalancer-securitygroups"></a>
\[Application Load Balancers\] The IDs of the security groups for the load balancer\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetMappings`  <a name="cfn-elasticloadbalancingv2-loadbalancer-subnetmappings"></a>
The IDs of the public subnets\. You can specify only one subnet per Availability Zone\. You must specify either subnets or subnet mappings\.  
\[Application Load Balancers\] You must specify subnets from at least two Availability Zones\. You cannot specify Elastic IP addresses for your subnets\.  
\[Application Load Balancers on Outposts\] You must specify one Outpost subnet\.  
\[Application Load Balancers on Local Zones\] You can specify subnets from one or more Local Zones\.  
\[Network Load Balancers\] You can specify subnets from one or more Availability Zones\. You can specify one Elastic IP address per subnet if you need static IP addresses for your internet\-facing load balancer\. For internal load balancers, you can specify one private IP address per subnet from the IPv4 range of the subnet\. For internet\-facing load balancer, you can specify one IPv6 address per subnet\.  
\[Gateway Load Balancers\] You can specify subnets from one or more Availability Zones\. You cannot specify Elastic IP addresses for your subnets\.  
*Required*: Conditional  
*Type*: List of [SubnetMapping](aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subnets`  <a name="cfn-elasticloadbalancingv2-loadbalancer-subnets"></a>
The IDs of the subnets\. You can specify only one subnet per Availability Zone\. You must specify either subnets or subnet mappings\.  
\[Application Load Balancers\] You must specify subnets from at least two Availability Zones\. When you specify subnets for an existing Application Load Balancer, they replace the previously enabled subnets\.  
\[Network Load Balancers\] You can specify subnets from one or more Availability Zones when you create the load balancer\. You can't change the subnets for an existing Network Load Balancer\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-elasticloadbalancingv2-loadbalancer-tags"></a>
The tags to assign to the load balancer\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-elasticloadbalancingv2-loadbalancer-type"></a>
The type of load balancer\. The default is `application`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `application | gateway | network`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-elasticloadbalancingv2-loadbalancer-return-values"></a>

### Ref<a name="aws-resource-elasticloadbalancingv2-loadbalancer-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the load balancer\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-elasticloadbalancingv2-loadbalancer-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-elasticloadbalancingv2-loadbalancer-return-values-fn--getatt-fn--getatt"></a>

`CanonicalHostedZoneID`  <a name="CanonicalHostedZoneID-fn::getatt"></a>
The ID of the Amazon Route 53 hosted zone associated with the load balancer\. For example, `Z2P70J7EXAMPLE`\.

`DNSName`  <a name="DNSName-fn::getatt"></a>
The DNS name for the load balancer\. For example, `my-load-balancer-424835706.us-west-2.elb.amazonaws.com`\.

`LoadBalancerFullName`  <a name="LoadBalancerFullName-fn::getatt"></a>
The full name of the load balancer\. For example, `app/my-load-balancer/50dc6c495c0c9188`\.

`LoadBalancerName`  <a name="LoadBalancerName-fn::getatt"></a>
The name of the load balancer\. For example, `my-load-balancer`\.

`SecurityGroups`  <a name="SecurityGroups-fn::getatt"></a>
The IDs of the security groups for the load balancer\.

## See also<a name="aws-resource-elasticloadbalancingv2-loadbalancer--seealso"></a>
+  [CreateLoadBalancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateLoadBalancer.html) in the *Elastic Load Balancing API Reference \(version 2015\-12\-01\)* 
+  [User Guide for Application Load Balancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/application) 
+  [User Guide for Network Load Balancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/network) 

