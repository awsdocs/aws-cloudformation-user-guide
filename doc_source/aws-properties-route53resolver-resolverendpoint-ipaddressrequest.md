# Amazon Route 53 ResolverEndpoint IpAddressRequest<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest"></a>

<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest-description"></a>The `IpAddressRequest` property type specifies the subnets and IP addresses in your VPC that you want DNS queries to pass through on the way from your VPCs to your network \(for outbound endpoints\) or on the way from your network to your VPCs \(for inbound resolver endpoints\)\.

<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest-inheritance"></a> `IpAddressRequest` is a property of the [AWS::Route53Resolver::ResolverEndpoint](aws-resource-route53resolver-resolverendpoint.md) resource\.

## Syntax<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest-syntax.json"></a>

```
{
  "[Ip](#cfn-route53resolver-resolverendpoint-ipaddressrequest-ip)" : String,
  "[SubnetId](#cfn-route53resolver-resolverendpoint-ipaddressrequest-subnetid)" : String
}
```

### YAML<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest-syntax.yaml"></a>

```
[Ip](#cfn-route53resolver-resolverendpoint-ipaddressrequest-ip): String
[SubnetId](#cfn-route53resolver-resolverendpoint-ipaddressrequest-subnetid): String
```

## Properties<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest-properties"></a>

`Ip`  <a name="cfn-route53resolver-resolverendpoint-ipaddressrequest-ip"></a>
The IP address that you want to use for DNS queries\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetId`  <a name="cfn-route53resolver-resolverendpoint-ipaddressrequest-subnetid"></a>
The subnet that contains the IP address\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest-seealso"></a>
+ [CreateResolverEndpoint](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_CreateResolverEndpoint.html) in the *Amazon Route 53 API Reference*