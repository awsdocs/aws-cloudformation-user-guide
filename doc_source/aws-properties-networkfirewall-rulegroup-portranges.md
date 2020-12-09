# AWS::NetworkFirewall::RuleGroup PortRanges<a name="aws-properties-networkfirewall-rulegroup-portranges"></a>

Port range specifications\. This is used for source and destination port specifications in the stateless [AWS::NetworkFirewall::RuleGroup MatchAttributes](aws-properties-networkfirewall-rulegroup-matchattributes.md)\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-portranges-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-portranges-syntax.json"></a>

```
{
  "[PortRanges](#cfn-networkfirewall-rulegroup-portranges-portranges)" : [ PortRange, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-portranges-syntax.yaml"></a>

```
  [PortRanges](#cfn-networkfirewall-rulegroup-portranges-portranges): 
    - PortRange
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-portranges-properties"></a>

`PortRanges`  <a name="cfn-networkfirewall-rulegroup-portranges-portranges"></a>
Port range specifications\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-portranges) of [PortRange](aws-properties-networkfirewall-rulegroup-portrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)