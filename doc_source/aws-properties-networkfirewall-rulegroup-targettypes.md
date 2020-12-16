# AWS::NetworkFirewall::RuleGroup TargetTypes<a name="aws-properties-networkfirewall-rulegroup-targettypes"></a>

The types of targets to inspect for\. 

## Syntax<a name="aws-properties-networkfirewall-rulegroup-targettypes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-targettypes-syntax.json"></a>

```
{
  "[TargetTypes](#cfn-networkfirewall-rulegroup-targettypes-targettypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-targettypes-syntax.yaml"></a>

```
  [TargetTypes](#cfn-networkfirewall-rulegroup-targettypes-targettypes): 
    - String
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-targettypes-properties"></a>

`TargetTypes`  <a name="cfn-networkfirewall-rulegroup-targettypes-targettypes"></a>
The types of targets to inspect for\. Valid values are `TLS_SNI` and `HTTP_HOST`\.   
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-targettypes) of [String](#aws-properties-networkfirewall-rulegroup-targettypes)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)