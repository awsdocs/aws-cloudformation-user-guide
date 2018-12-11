# AWS::Route53Resolver::ResolverEndpoint<a name="aws-resource-route53resolver-resolverendpoint"></a>

The `AWS::Route53Resolver::ResolverEndpoint` resource includes settings for inbound or outbound endpoints for Amazon Route 53\. For more information, see [ResolverEndpoint](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverEndpoint.html) in the *Amazon Route 53 API Reference*\. 

## Syntax<a name="aws-resource-route53resolver-resolverendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-resolverendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverEndpoint",
  "Properties" : {
    "[Direction](#cfn-route53resolver-resolverendpoint-direction)" : String,
    "[IpAddresses](#cfn-route53resolver-resolverendpoint-ipaddresses)" : [ [*IpAddressRequest*](aws-properties-route53resolver-resolverendpoint-ipaddressrequest.md), ... ],
    "[Name](#cfn-route53resolver-resolverendpoint-name)" : String,
    "[SecurityGroupIds](#cfn-route53resolver-resolverendpoint-securitygroupids)" : [ String, ... ],
    "[Tags](#cfn-route53resolver-resolverendpoint-tags)" : [ [*Resource Tag*](aws-properties-resource-tags.md), ... ]
  }
}
```

### YAML<a name="aws-resource-route53resolver-resolverendpoint-syntax.yaml"></a>

```
Type: "AWS::Route53Resolver::ResolverEndpoint"
Properties:
  [Direction](#cfn-route53resolver-resolverendpoint-direction): String
  [IpAddresses](#cfn-route53resolver-resolverendpoint-ipaddresses): 
    - [*IpAddressRequest*](aws-properties-route53resolver-resolverendpoint-ipaddressrequest.md)
  [Name](#cfn-route53resolver-resolverendpoint-name): String
  [SecurityGroupIds](#cfn-route53resolver-resolverendpoint-securitygroupids): 
    - String
  [Tags](#cfn-route53resolver-resolverendpoint-tags): 
    - [*Resource Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-resource-route53resolver-resolverendpoint-properties"></a>

`Direction`  <a name="cfn-route53resolver-resolverendpoint-direction"></a>
Indicates whether the resolver endpoint allows inbound or outbound DNS queries\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`IpAddresses`  <a name="cfn-route53resolver-resolverendpoint-ipaddresses"></a>
The subnets and IP addresses in your VPC that you want DNS queries to pass through on the way from your VPCs to your network \(for outbound endpoints\) or on the way from your network to your VPCs \(for inbound resolver endpoints\)\.   
 *Required*: Yes  
 *Type*: List of [IpAddressRequest](aws-properties-route53resolver-resolverendpoint-ipaddressrequest.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-route53resolver-resolverendpoint-name"></a>
A friendly name that lets you easily find a configuration in the Resolver dashboard in the Route 53 console\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecurityGroupIds`  <a name="cfn-route53resolver-resolverendpoint-securitygroupids"></a>
The ID of one or more security groups that you want to use to control access to this VPC\. The security group that you specify must include one or more inbound rules \(for inbound resolver endpoints\) or outbound rules \(for outbound resolver endpoints\)\.   
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-route53resolver-resolverendpoint-tags"></a>
A list of the tag keys and values that you want to associate with the endpoint\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-route53resolver-resolverendpoint-returnvalues"></a>

### Ref<a name="aws-resource-route53resolver-resolverendpoint-ref"></a>

When you pass the logical ID of an `AWS::Route53Resolver::ResolverEndpoint` resource to the intrinsic `Ref` function, the function returns the `ResolverEndpoint` object\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverendpoint-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the resolver endpoint, such as `arn:aws:route53Resolver:us-east-1:123456789012:resolver-endpoint/resolver-endpoint-a1bzhi`\.

`Direction`  
Indicates whether the resolver endpoint allows inbound or outbound DNS queries\.

`HostVPCId`  
The ID of the VPC that you want to create the resolver endpoint in\.

`IpAddressCount`  
The number of IP addresses that the resolver endpoint can use for DNS queries\.

`Name`  
The name that you assigned to the resolver endpoint when you created the endpoint\. 

`ResolverEndpointId`  
The ID of the resolver endpoint\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## See Also<a name="aws-resource-route53resolver-resolverendpoint-seealso"></a>
+ [ResolverEndpoint](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverEndpoint.html) in the *Amazon Route 53 API Reference*