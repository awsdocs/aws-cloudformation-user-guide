# Amazon Route 53 ResolverRule TargetAddress<a name="aws-properties-route53resolver-resolverrule-targetaddress"></a>

<a name="aws-properties-route53resolver-resolverrule-targetaddress-description"></a>The `TargetAddress` property type specifies the IP addresses that you want Resolver to forward DNS queries to\. These are typically the IP addresses of DNS resolvers in your network\.

<a name="aws-properties-route53resolver-resolverrule-targetaddress-inheritance"></a> `TargetAddress` is a property of the [AWS::Route53Resolver::ResolverRule](aws-resource-route53resolver-resolverrule.md) resource\.

## Syntax<a name="aws-properties-route53resolver-resolverrule-targetaddress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53resolver-resolverrule-targetaddress-syntax.json"></a>

```
{
  "[Ip](#cfn-route53resolver-resolverrule-targetaddress-ip)" : String,
  "[Port](#cfn-route53resolver-resolverrule-targetaddress-port)" : String
}
```

### YAML<a name="aws-properties-route53resolver-resolverrule-targetaddress-syntax.yaml"></a>

```
[Ip](#cfn-route53resolver-resolverrule-targetaddress-ip): String
[Port](#cfn-route53resolver-resolverrule-targetaddress-port): String
```

## Properties<a name="aws-properties-route53resolver-resolverrule-targetaddress-properties"></a>

`Ip`  <a name="cfn-route53resolver-resolverrule-targetaddress-ip"></a>
One IP address that you want to forward DNS queries to\. You can specify only IPv4 addresses\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Port`  <a name="cfn-route53resolver-resolverrule-targetaddress-port"></a>
The port at `Ip` that you want to forward DNS queries to\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-route53resolver-resolverrule-targetaddress-seealso"></a>
+ [CreateResolverRule](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_CreateResolverRule.html) in the *Amazon Route 53 API Reference*