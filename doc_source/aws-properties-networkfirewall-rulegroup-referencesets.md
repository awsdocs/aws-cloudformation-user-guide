# AWS::NetworkFirewall::RuleGroup ReferenceSets<a name="aws-properties-networkfirewall-rulegroup-referencesets"></a>

Configures the [ReferenceSets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-networkfirewall-rulegroup-rulegroup.html#cfn-networkfirewall-rulegroup-rulegroup-referencesets) for a stateful rule group\. For more information, see the [Using IP set references in Suricata compatible rule groups](https://docs.aws.amazon.com/network-firewall/latest/developerguide/rule-groups-ip-set-references.html) in the *Network Firewall User Guide*\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-referencesets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-referencesets-syntax.json"></a>

```
{
  "[IPSetReferences](#cfn-networkfirewall-rulegroup-referencesets-ipsetreferences)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-referencesets-syntax.yaml"></a>

```
  [IPSetReferences](#cfn-networkfirewall-rulegroup-referencesets-ipsetreferences): 
    Key : Value
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-referencesets-properties"></a>

`IPSetReferences`  <a name="cfn-networkfirewall-rulegroup-referencesets-ipsetreferences"></a>
The IP set references to use in the stateful rule group\.  
*Required*: No  
*Type*: Map of [IPSetReference](aws-properties-networkfirewall-rulegroup-ipsetreference.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)