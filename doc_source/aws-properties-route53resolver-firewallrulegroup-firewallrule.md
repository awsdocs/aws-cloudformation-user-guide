# AWS::Route53Resolver::FirewallRuleGroup FirewallRule<a name="aws-properties-route53resolver-firewallrulegroup-firewallrule"></a>

A single firewall rule in a rule group\.

## Syntax<a name="aws-properties-route53resolver-firewallrulegroup-firewallrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53resolver-firewallrulegroup-firewallrule-syntax.json"></a>

```
{
  "[Action](#cfn-route53resolver-firewallrulegroup-firewallrule-action)" : String,
  "[BlockOverrideDnsType](#cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridednstype)" : String,
  "[BlockOverrideDomain](#cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridedomain)" : String,
  "[BlockOverrideTtl](#cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridettl)" : Integer,
  "[BlockResponse](#cfn-route53resolver-firewallrulegroup-firewallrule-blockresponse)" : String,
  "[FirewallDomainListId](#cfn-route53resolver-firewallrulegroup-firewallrule-firewalldomainlistid)" : String,
  "[Priority](#cfn-route53resolver-firewallrulegroup-firewallrule-priority)" : Integer
}
```

### YAML<a name="aws-properties-route53resolver-firewallrulegroup-firewallrule-syntax.yaml"></a>

```
  [Action](#cfn-route53resolver-firewallrulegroup-firewallrule-action): String
  [BlockOverrideDnsType](#cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridednstype): String
  [BlockOverrideDomain](#cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridedomain): String
  [BlockOverrideTtl](#cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridettl): Integer
  [BlockResponse](#cfn-route53resolver-firewallrulegroup-firewallrule-blockresponse): String
  [FirewallDomainListId](#cfn-route53resolver-firewallrulegroup-firewallrule-firewalldomainlistid): String
  [Priority](#cfn-route53resolver-firewallrulegroup-firewallrule-priority): Integer
```

## Properties<a name="aws-properties-route53resolver-firewallrulegroup-firewallrule-properties"></a>

`Action`  <a name="cfn-route53resolver-firewallrulegroup-firewallrule-action"></a>
The action that DNS Firewall should take on a DNS query when it matches one of the domains in the rule's domain list:  
+  `ALLOW` \- Permit the request to go through\.
+  `ALERT` \- Permit the request to go through but send an alert to the logs\.
+  `BLOCK` \- Disallow the request\. If this is specified,then `BlockResponse` must also be specified\.

  if `BlockResponse` is `OVERRIDE`, then all of the following `OVERRIDE` attributes must be specified:
  + `BlockOverrideDnsType` 
  + `BlockOverrideDomain`
  + `BlockOverrideTtl`
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALERT | ALLOW | BLOCK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlockOverrideDnsType`  <a name="cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridednstype"></a>
The DNS record's type\. This determines the format of the record value that you provided in `BlockOverrideDomain`\. Used for the rule action `BLOCK` with a `BlockResponse` setting of `OVERRIDE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CNAME`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlockOverrideDomain`  <a name="cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridedomain"></a>
The custom DNS record to send back in response to the query\. Used for the rule action `BLOCK` with a `BlockResponse` setting of `OVERRIDE`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlockOverrideTtl`  <a name="cfn-route53resolver-firewallrulegroup-firewallrule-blockoverridettl"></a>
The recommended amount of time, in seconds, for the DNS resolver or web browser to cache the provided override record\. Used for the rule action `BLOCK` with a `BlockResponse` setting of `OVERRIDE`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlockResponse`  <a name="cfn-route53resolver-firewallrulegroup-firewallrule-blockresponse"></a>
The way that you want DNS Firewall to block the request\. Used for the rule action setting `BLOCK`\.  
+  `NODATA` \- Respond indicating that the query was successful, but no response is available for it\.
+  `NXDOMAIN` \- Respond indicating that the domain name that's in the query doesn't exist\.
+  `OVERRIDE` \- Provide a custom override in the response\. This option requires custom handling details in the rule's `BlockOverride*` settings\. 
*Required*: No  
*Type*: String  
*Allowed values*: `NODATA | NXDOMAIN | OVERRIDE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirewallDomainListId`  <a name="cfn-route53resolver-firewallrulegroup-firewallrule-firewalldomainlistid"></a>
The ID of the domain list that's used in the rule\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-route53resolver-firewallrulegroup-firewallrule-priority"></a>
The priority of the rule in the rule group\. This value must be unique within the rule group\. DNS Firewall processes the rules in a rule group by order of priority, starting from the lowest setting\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)