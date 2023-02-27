# AWS::WAFv2::RuleGroup ImmunityTimeProperty<a name="aws-properties-wafv2-rulegroup-immunitytimeproperty"></a>

Used for CAPTCHA and challenge token settings\. Determines how long a `CAPTCHA` or challenge timestamp remains valid after AWS WAF updates it for a successful `CAPTCHA` or challenge response\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-immunitytimeproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-immunitytimeproperty-syntax.json"></a>

```
{
  "[ImmunityTime](#cfn-wafv2-rulegroup-immunitytimeproperty-immunitytime)" : Integer
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-immunitytimeproperty-syntax.yaml"></a>

```
  [ImmunityTime](#cfn-wafv2-rulegroup-immunitytimeproperty-immunitytime): Integer
```

## Properties<a name="aws-properties-wafv2-rulegroup-immunitytimeproperty-properties"></a>

`ImmunityTime`  <a name="cfn-wafv2-rulegroup-immunitytimeproperty-immunitytime"></a>
The amount of time, in seconds, that a `CAPTCHA` or challenge timestamp is considered valid by AWS WAF\. The default setting is 300\.   
For the Challenge action, the minimum setting is 300\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)