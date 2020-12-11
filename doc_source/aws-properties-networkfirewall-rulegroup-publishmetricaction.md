# AWS::NetworkFirewall::RuleGroup PublishMetricAction<a name="aws-properties-networkfirewall-rulegroup-publishmetricaction"></a>

Stateless inspection criteria that publishes the specified metrics to Amazon CloudWatch for the matching packet\. This setting defines a CloudWatch dimension value to be published\.

## Syntax<a name="aws-properties-networkfirewall-rulegroup-publishmetricaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkfirewall-rulegroup-publishmetricaction-syntax.json"></a>

```
{
  "[Dimensions](#cfn-networkfirewall-rulegroup-publishmetricaction-dimensions)" : Dimensions
}
```

### YAML<a name="aws-properties-networkfirewall-rulegroup-publishmetricaction-syntax.yaml"></a>

```
  [Dimensions](#cfn-networkfirewall-rulegroup-publishmetricaction-dimensions): 
    Dimensions
```

## Properties<a name="aws-properties-networkfirewall-rulegroup-publishmetricaction-properties"></a>

`Dimensions`  <a name="cfn-networkfirewall-rulegroup-publishmetricaction-dimensions"></a>
  
*Required*: Yes  
*Type*: [Dimensions](aws-properties-networkfirewall-rulegroup-dimensions.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)