# AWS::Route53Resolver::ResolverRule TargetAddress<a name="aws-properties-route53resolver-resolverrule-targetaddress"></a>

In a [CreateResolverRule](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_CreateResolverRule.html) request, an array of the IPs that you want to forward DNS queries to\.

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
*Minimum*: `7`  
*Maximum*: `36`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-route53resolver-resolverrule-targetaddress-port"></a>
The port at `Ip` that you want to forward DNS queries to\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-route53resolver-resolverrule-targetaddress--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html#aws-resource-route53resolver-resolverrule-return-values) in the topic [AWS::Route53Resolver::ResolverRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html) 
+  [TargetAddress](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_TargetAddress.html) in the *Amazon Route 53 API Reference* 

