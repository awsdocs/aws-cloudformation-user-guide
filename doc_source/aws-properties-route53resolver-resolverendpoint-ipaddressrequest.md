# AWS::Route53Resolver::ResolverEndpoint IpAddressRequest<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest"></a>

In a [CreateResolverEndpoint](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_CreateResolverEndpoint.html) request, the IP address that DNS queries originate from \(for outbound endpoints\) or that you forward DNS queries to \(for inbound endpoints\)\. `IpAddressRequest` also includes the ID of the subnet that contains the IP address\.

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
*Minimum*: `7`  
*Maximum*: `36`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-route53resolver-resolverendpoint-ipaddressrequest-subnetid"></a>
The ID of the subnet that contains the IP address\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-route53resolver-resolverendpoint-ipaddressrequest--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html#aws-resource-route53resolver-resolverendpoint-return-values) in the topic [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html) 
+  [IpAddressRequest](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_IpAddressRequest.html) in the *Amazon Route 53 API Reference* 

