# AWS::NetworkFirewall::RuleGroup TCPFlags<a name="aws-properties-networkfirewall-rulegroup-tcpflags"></a>

The TCP flags and masks to inspect for\. If not specified, this matches with any settings\. This setting is only used for protocol 6 \(TCP\)\. This is used in the [AWS::NetworkFirewall::RuleGroup MatchAttributes](aws-properties-networkfirewall-rulegroup-matchattributes.md) specification\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-tcpflags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-tcpflags-syntax.json"></a>

```
{
  "[TCPFlags](#cfn-networkfirewall-rulegroup-tcpflags-tcpflags)" : [ TCPFlagField, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-tcpflags-syntax.yaml"></a>

```
  [TCPFlags](#cfn-networkfirewall-rulegroup-tcpflags-tcpflags): 
    - TCPFlagField
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-tcpflags-properties"></a>

`TCPFlags`  <a name="cfn-networkfirewall-rulegroup-tcpflags-tcpflags"></a>
The TCP flags and masks to inspect for\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-tcpflags) of [TCPFlagField](aws-properties-networkfirewall-rulegroup-tcpflagfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)