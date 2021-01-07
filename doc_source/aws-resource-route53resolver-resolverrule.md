# AWS::Route53Resolver::ResolverRule<a name="aws-resource-route53resolver-resolverrule"></a>

For DNS queries that originate in your VPCs, specifies which Resolver endpoint the queries pass through, one domain name that you want to forward to your network, and the IP addresses of the DNS resolvers in your network\.

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
      "[Tags](#cfn-route53resolver-resolverrule-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetIps](#cfn-route53resolver-resolverrule-targetips)" : [ TargetAddress, ... ]
    }
}
```

### YAML<a name="aws-resource-route53resolver-resolverrule-syntax.yaml"></a>

```
Type: AWS::Route53Resolver::ResolverRule
Properties: 
  [DomainName](#cfn-route53resolver-resolverrule-domainname): String
  [Name](#cfn-route53resolver-resolverrule-name): String
  [ResolverEndpointId](#cfn-route53resolver-resolverrule-resolverendpointid): String
  [RuleType](#cfn-route53resolver-resolverrule-ruletype): String
  [Tags](#cfn-route53resolver-resolverrule-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetIps](#cfn-route53resolver-resolverrule-targetips): 
    - TargetAddress
```

## Properties<a name="aws-resource-route53resolver-resolverrule-properties"></a>

`DomainName`  <a name="cfn-route53resolver-resolverrule-domainname"></a>
DNS queries for this domain name are forwarded to the IP addresses that are specified in `TargetIps`\. If a query matches multiple Resolver rules \(example\.com and www\.example\.com\), the query is routed using the Resolver rule that contains the most specific domain name \(www\.example\.com\)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-route53resolver-resolverrule-name"></a>
The name for the Resolver rule, which you specified when you created the Resolver rule\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `(?!^[0-9]+$)([a-zA-Z0-9\-_' ']+)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResolverEndpointId`  <a name="cfn-route53resolver-resolverrule-resolverendpointid"></a>
The ID of the endpoint that the rule is associated with\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleType`  <a name="cfn-route53resolver-resolverrule-ruletype"></a>
When you want to forward DNS queries for specified domain name to resolvers on your network, specify `FORWARD`\.  
When you have a forwarding rule to forward DNS queries for a domain to your network and you want Resolver to process queries for a subdomain of that domain, specify `SYSTEM`\.  
For example, to forward DNS queries for example\.com to resolvers on your network, you create a rule and specify `FORWARD` for `RuleType`\. To then have Resolver process queries for apex\.example\.com, you create a rule and specify `SYSTEM` for `RuleType`\.  
Currently, only Resolver can create rules that have a value of `RECURSIVE` for `RuleType`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FORWARD | RECURSIVE | SYSTEM`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-route53resolver-resolverrule-tags"></a>
A list of the tag keys and values that you want to associate with the endpoint\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetIps`  <a name="cfn-route53resolver-resolverrule-targetips"></a>
An array that contains the IP addresses and ports that an outbound endpoint forwards DNS queries to\. Typically, these are the IP addresses of DNS resolvers on your network\. Specify IPv4 addresses\. IPv6 is not supported\.  
*Required*: No  
*Type*: List of [TargetAddress](aws-properties-route53resolver-resolverrule-targetaddress.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53resolver-resolverrule-return-values"></a>

### Ref<a name="aws-resource-route53resolver-resolverrule-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ResolverRule` object, which contains detailed information about the rule\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverrule-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53resolver-resolverrule-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the resolver rule, such as `arn:aws:route53Resolver:us-east-1:123456789012:resolver-rule/resolver-rule-a1bzhi`\.

`DomainName`  <a name="DomainName-fn::getatt"></a>
DNS queries for this domain name are forwarded to the IP addresses that are specified in TargetIps\. If a query matches multiple resolver rules \(example\.com and www\.example\.com\), the query is routed using the resolver rule that contains the most specific domain name \(www\.example\.com\)\.

`Name`  <a name="Name-fn::getatt"></a>
A friendly name that lets you easily find a rule in the Resolver dashboard in the Route 53 console\. 

`ResolverEndpointId`  <a name="ResolverEndpointId-fn::getatt"></a>
The ID of the outbound endpoint that the rule is associated with, such as `rslvr-out-fdc049932dexample`\.

`ResolverRuleId`  <a name="ResolverRuleId-fn::getatt"></a>
When the value of `RuleType` is `FORWARD`, the ID that Resolver assigned to the resolver rule when you created it, such as `rslvr-rr-5328a0899aexample`\. This value isn't applicable when `RuleType` is `SYSTEM`\.

`TargetIps`  <a name="TargetIps-fn::getatt"></a>
When the value of `RuleType` is `FORWARD`, the IP addresses that the outbound endpoint forwards DNS queries to, typically the IP addresses for DNS resolvers on your network\. This value isn't applicable when `RuleType` is `SYSTEM`\.

## Examples<a name="aws-resource-route53resolver-resolverrule--examples"></a>



### Create Resolver rule<a name="aws-resource-route53resolver-resolverrule--examples--Create_Resolver_rule"></a>

The following example creates an Amazon Route 53 outbound resolver rule\.

#### JSON<a name="aws-resource-route53resolver-resolverrule--examples--Create_Resolver_rule--json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverRule",
  "Properties" : {
    "DomainName" : "example.com",
    "Name" : "MyRule",
    "ResolverEndpointId" : "rslvr-out-fdc049932dexample",
    "RuleType" : "FORWARD", 
    "Tags" : [
      {
        "Key": "LineOfBusiness",
        "Value": "Engineering"
      }
    ],
    "TargetIps" : [
      {
        "Ip" : "192.0.2.6",
        "Port" : "53"
      },
      {
        "Ip" : "192.0.2.99,
        "Port" : "53"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-route53resolver-resolverrule--examples--Create_Resolver_rule--yaml"></a>

```
Type : AWS::Route53Resolver::ResolverRule
Properties : 
  DomainName : example.com
  Name : MyRule
  ResolverEndpointId : rslvr-out-fdc049932dexample
  RuleType : FORWARD 
  Tags : 
    - 
      Key : LineOfBusiness
      Value : Engineering
  TargetIps :
    - 
      Ip : 192.0.2.6
      Port : 53
    -  
      Ip : 192.0.2.99
      Port : 53
```

## See also<a name="aws-resource-route53resolver-resolverrule--seealso"></a>
+  [ResolverRule](https://docs.aws.amazon.com/Route53/latest/APIReference/API_route53resolver_ResolverRule.html) in the *Amazon Route 53 API Reference* 

