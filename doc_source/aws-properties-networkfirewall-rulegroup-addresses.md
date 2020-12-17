# AWS::NetworkFirewall::RuleGroup Addresses<a name="aws-properties-networkfirewall-rulegroup-addresses"></a>

IP address specifications\. This is used in the [AWS::NetworkFirewall::RuleGroup MatchAttributes](aws-properties-networkfirewall-rulegroup-matchattributes.md) source and destination specifications\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-addresses-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-addresses-syntax.json"></a>

```
{
  "[Addresses](#cfn-networkfirewall-rulegroup-addresses-addresses)" : [ Address, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-addresses-syntax.yaml"></a>

```
  [Addresses](#cfn-networkfirewall-rulegroup-addresses-addresses): 
    - Address
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-addresses-properties"></a>

`Addresses`  <a name="cfn-networkfirewall-rulegroup-addresses-addresses"></a>
IP address specifications\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-addresses) of [Address](aws-properties-networkfirewall-rulegroup-address.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)