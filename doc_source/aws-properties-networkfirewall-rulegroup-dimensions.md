# AWS::NetworkFirewall::RuleGroup Dimensions<a name="aws-properties-networkfirewall-rulegroup-dimensions"></a>

Array of dimension objects\. This is used in the [AWS::NetworkFirewall::RuleGroup PublishMetricAction](aws-properties-networkfirewall-rulegroup-publishmetricaction.md) specification\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-dimensions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-dimensions-syntax.json"></a>

```
{
  "[Dimensions](#cfn-networkfirewall-rulegroup-dimensions-dimensions)" : [ Dimension, ... ]
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-dimensions-syntax.yaml"></a>

```
  [Dimensions](#cfn-networkfirewall-rulegroup-dimensions-dimensions): 
    - Dimension
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-dimensions-properties"></a>

`Dimensions`  <a name="cfn-networkfirewall-rulegroup-dimensions-dimensions"></a>
Array of dimension objects\.  
*Required*: No  
*Type*: [List](#aws-properties-networkfirewall-rulegroup-dimensions) of [Dimension](aws-properties-networkfirewall-rulegroup-dimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)