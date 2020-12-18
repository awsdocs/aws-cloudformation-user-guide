# AWS::NetworkFirewall::RuleGroup Flags<a name="aws-properties-networkfirewall-rulegroup-flags"></a>

A set of flags, used for the `Flags` and `Masks` settings in a [AWS::NetworkFirewall::RuleGroup TCPFlagField](aws-properties-networkfirewall-rulegroup-tcpflagfield.md)\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-flags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-flags-syntax.json"></a>

```
{
  "[Flags](#cfn-networkfirewall-rulegroup-flags-flags)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-flags-syntax.yaml"></a>

```
  [Flags](#cfn-networkfirewall-rulegroup-flags-flags): 
    - String
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-flags-properties"></a>

`Flags`  <a name="cfn-networkfirewall-rulegroup-flags-flags"></a>
A set of flags, used for the `Flags` and `Masks` settings in a [AWS::NetworkFirewall::RuleGroup TCPFlagField](aws-properties-networkfirewall-rulegroup-tcpflagfield.md)\.  
Valid values are the following: `FIN` \| `SYN` \| `RST` \| `PSH` \| `ACK` \| `URG` \| `ECE` \| `CWR`  
For example, `[ "FIN", "RST" ]`\.  
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-flags) of [String](#aws-properties-networkfirewall-rulegroup-flags)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)