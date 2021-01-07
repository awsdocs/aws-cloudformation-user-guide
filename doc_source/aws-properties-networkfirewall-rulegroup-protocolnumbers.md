# AWS::NetworkFirewall::RuleGroup ProtocolNumbers<a name="aws-properties-networkfirewall-rulegroup-protocolnumbers"></a>

Protocol specifications\. This is used in the stateless [AWS::NetworkFirewall::RuleGroup MatchAttributes](aws-properties-networkfirewall-rulegroup-matchattributes.md)\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-protocolnumbers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-protocolnumbers-syntax.json"></a>

```
{
  "[ProtocolNumbers](#cfn-networkfirewall-rulegroup-protocolnumbers-protocolnumbers)" : [ Integer, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-protocolnumbers-syntax.yaml"></a>

```
  [ProtocolNumbers](#cfn-networkfirewall-rulegroup-protocolnumbers-protocolnumbers): 
    - Integer
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-protocolnumbers-properties"></a>

`ProtocolNumbers`  <a name="cfn-networkfirewall-rulegroup-protocolnumbers-protocolnumbers"></a>
Protocols, specified using each protocol's assigned internet protocol number \(IANA\)\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-protocolnumbers) of [Integer](#aws-properties-networkfirewall-rulegroup-protocolnumbers)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)