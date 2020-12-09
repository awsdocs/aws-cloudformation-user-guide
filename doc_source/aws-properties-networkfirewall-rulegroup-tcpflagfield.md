# AWS::NetworkFirewall::RuleGroup TCPFlagField<a name="aws-properties-networkfirewall-rulegroup-tcpflagfield"></a>

TCP flags and masks to inspect packets for\. This is used in the [AWS::NetworkFirewall::RuleGroup MatchAttributes](aws-properties-networkfirewall-rulegroup-matchattributes.md) specification\.

For example:

`"TCPFlags": [ { "Flags": [ "ECE", "SYN" ], "Masks": [ "SYN", "ECE" ] } ]`

## Syntax<a name="aws-properties-networkfirewall-rulegroup-tcpflagfield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-tcpflagfield-syntax.json"></a>

```
{
  "[Flags](#cfn-networkfirewall-rulegroup-tcpflagfield-flags)" : Flags,
  "[Masks](#cfn-networkfirewall-rulegroup-tcpflagfield-masks)" : Flags
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-tcpflagfield-syntax.yaml"></a>

```
  [Flags](#cfn-networkfirewall-rulegroup-tcpflagfield-flags): 
    Flags
  [Masks](#cfn-networkfirewall-rulegroup-tcpflagfield-masks): 
    Flags
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-tcpflagfield-properties"></a>

`Flags`  <a name="cfn-networkfirewall-rulegroup-tcpflagfield-flags"></a>
Used in conjunction with the `Masks` setting to define the flags that must be set and flags that must not be set in order for the packet to match\. This setting can only specify values that are also specified in the `Masks` setting\.  
For the flags that are specified in the masks setting, the following must be true for the packet to match:   
+ The ones that are set in this flags setting must be set in the packet\. 
+ The ones that are not set in this flags setting must also not be set in the packet\. 
*Required*: Yes  
*Type*: [Flags](aws-properties-networkfirewall-rulegroup-flags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Masks`  <a name="cfn-networkfirewall-rulegroup-tcpflagfield-masks"></a>
The set of flags to consider in the inspection\. To inspect all flags in the valid values list, leave this with no setting\.  
*Required*: No  
*Type*: [Flags](aws-properties-networkfirewall-rulegroup-flags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)