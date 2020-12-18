# AWS::NetworkFirewall::RuleGroup RulesSourceList<a name="aws-properties-networkfirewall-rulegroup-rulessourcelist"></a>

Stateful inspection criteria for a domain list rule group\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-rulessourcelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-rulessourcelist-syntax.json"></a>

```
{
  "[GeneratedRulesType](#cfn-networkfirewall-rulegroup-rulessourcelist-generatedrulestype)" : String,
  "[Targets](#cfn-networkfirewall-rulegroup-rulessourcelist-targets)" : [ String, ... ],
  "[TargetTypes](#cfn-networkfirewall-rulegroup-rulessourcelist-targettypes)" : TargetTypes
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-rulessourcelist-syntax.yaml"></a>

```
  [GeneratedRulesType](#cfn-networkfirewall-rulegroup-rulessourcelist-generatedrulestype): String
  [Targets](#cfn-networkfirewall-rulegroup-rulessourcelist-targets): 
    - String
  [TargetTypes](#cfn-networkfirewall-rulegroup-rulessourcelist-targettypes): 
    TargetTypes
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-rulessourcelist-properties"></a>

`GeneratedRulesType`  <a name="cfn-networkfirewall-rulegroup-rulessourcelist-generatedrulestype"></a>
Whether you want to allow or deny access to the domains in your target list\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALLOWLIST | DENYLIST`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-networkfirewall-rulegroup-rulessourcelist-targets"></a>
The domains that you want to inspect for in your traffic flows\. To provide multiple domains, separate them with commas\. Valid domain specifications are the following:  
+ Explicit names\. For example, `abc.example.com` matches only the domain `abc.example.com`\.
+ Names that use a domain wildcard, which you indicate with an initial '`.`'\. For example,`.example.com` matches `example.com` and matches all subdomains of `example.com`, such as `abc.example.com` and `www.example.com`\. 
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTypes`  <a name="cfn-networkfirewall-rulegroup-rulessourcelist-targettypes"></a>
The types of targets to inspect for\. Valid values are `TLS_SNI` and `HTTP_HOST`\.   
*Required*: Yes  
*Type*: [TargetTypes](aws-properties-networkfirewall-rulegroup-targettypes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)