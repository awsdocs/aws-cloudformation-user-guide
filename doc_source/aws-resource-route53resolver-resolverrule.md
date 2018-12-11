# AWS::Route53Resolver::ResolverRule<a name="aws-resource-route53resolver-resolverrule"></a>

The `AWS::Route53Resolver::ResolverRule` resource provides detailed information about a resolver rule, which specifies how to route DNS queries out of a VPC for Amazon Route 53 Resolver\. For more information, see [ResolverRule](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverRule.html) in the *Amazon Route 53 API Reference*\. 

## Syntax<a name="aws-resource-route53resolver-resolverrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-resolverrule-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverRule",
  "Properties" : {
    "[DomainName](#cfn-route53resolver-resolverrule-domainname)" : String,
    "[Name](#cfn-route53resolver-resolverrule-name)" : String,
    "[ResolverEndpointId](#cfn-route53resolver-resolverrule-resolverendpointid)" : String,
    "[RuleType](#cfn-route53resolver-resolverrule-ruletype)" : String,
    "[Tags](#cfn-route53resolver-resolverrule-tags)" : [ [*Resource Tag*](aws-properties-resource-tags.md), ... ],
    "[TargetIps](#cfn-route53resolver-resolverrule-targetips)" : [ [*TargetAddress*](aws-properties-route53resolver-resolverrule-targetaddress.md), ... ]
  }
}
```

### YAML<a name="aws-resource-route53resolver-resolverrule-syntax.yaml"></a>

```
Type: "AWS::Route53Resolver::ResolverRule"
Properties:
  [DomainName](#cfn-route53resolver-resolverrule-domainname): String
  [Name](#cfn-route53resolver-resolverrule-name): String
  [ResolverEndpointId](#cfn-route53resolver-resolverrule-resolverendpointid): String
  [RuleType](#cfn-route53resolver-resolverrule-ruletype): String
  [Tags](#cfn-route53resolver-resolverrule-tags): 
    - [*Resource Tag*](aws-properties-resource-tags.md)
  [TargetIps](#cfn-route53resolver-resolverrule-targetips): 
    - [*TargetAddress*](aws-properties-route53resolver-resolverrule-targetaddress.md)
```

## Properties<a name="aws-resource-route53resolver-resolverrule-properties"></a>

`DomainName`  <a name="cfn-route53resolver-resolverrule-domainname"></a>
DNS queries for this domain name are forwarded to the IP addresses that are specified in TargetIps\. If a query matches multiple resolver rules \(example\.com and www\.example\.com\), the query is routed using the resolver rule that contains the most specific domain name \(www\.example\.com\)\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-route53resolver-resolverrule-name"></a>
A friendly name that lets you easily find a rule in the Resolver dashboard in the Route 53 console\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResolverEndpointId`  <a name="cfn-route53resolver-resolverrule-resolverendpointid"></a>
The ID of the outbound endpoint that the rule is associated with\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RuleType`  <a name="cfn-route53resolver-resolverrule-ruletype"></a>
When you want to forward DNS queries for specified domain name to resolvers on your network, specify `FORWARD`\.  
When you have a forwarding rule to forward DNS queries for a domain to your network and you want Resolver to process queries for a subdomain of that domain, choose `SYSTEM`\.  
For example, to forward DNS queries for example\.com to resolvers on your network, you create a rule and specify `FORWARD` for `RuleType`\. To then have Resolver process queries for apex\.example\.com, you create a rule and specify `SYSTEM` for `RuleType`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-route53resolver-resolverrule-tags"></a>
A list of the tag keys and values that you want to associate with the rule\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetIps`  <a name="cfn-route53resolver-resolverrule-targetips"></a>
When a DNS query matches the name that you specify in `DomainName`, the outbound endpoint forwards the query to the IP addresses that you specify here, typically the IP addresses for DNS resolvers on your network\. Specify IPv4 addresses\. IPv6 is not supported\.   
 *Required*: No  
 *Type*: List of [TargetAddress](aws-properties-route53resolver-resolverrule-targetaddress.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-route53resolver-resolverrule-returnvalues"></a>

### Ref<a name="aws-resource-route53resolver-resolverrule-ref"></a>

When you pass the logical ID of an `AWS::Route53Resolver::ResolverRule` resource to the intrinsic `Ref` function, the function returns the `ResolverRule` object, which contains detailed information about the rule\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverrule-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the resolver rule, such as `arn:aws:route53Resolver:us-east-1:123456789012:resolver-rule/resolver-rule-a1bzhi`\.

`DomainName`  
DNS queries for this domain name are forwarded to the IP addresses that are specified in TargetIps\. If a query matches multiple resolver rules \(example\.com and www\.example\.com\), the query is routed using the resolver rule that contains the most specific domain name \(www\.example\.com\)\. 

`ResolverEndpointId`  
The ID of the outbound endpoint that the rule is associated with, such as `rslvr-out-fdc049932dexample`\.

`ResolverRuleId`  
When the value of `RuleType` is `FORWARD`, the ID that Resolver assigned to the resolver rule when you created it, such as `rslvr-rr-5328a0899aexample`\. This value isn't applicable when `RuleType` is `SYSTEM`\.

`TargetIps`  
When the value of `RuleType` is `FORWARD`, the IP addresses that the outbound endpoint forwards DNS queries to, typically the IP addresses for DNS resolvers on your network\. This value isn't applicable when `RuleType` is `SYSTEM`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## See Also<a name="aws-resource-route53resolver-resolverrule-seealso"></a>
+ [ResolverRule](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverRule.html) in the *Amazon Route 53 API Reference*\.