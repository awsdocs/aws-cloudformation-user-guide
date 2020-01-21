# AWS::WAFv2::RuleGroup CountryCodes<a name="aws-properties-wafv2-rulegroup-countrycodes"></a>

An array of two\-character country codes, for example, \[ "US", "CN" \], from the alpha\-2 country ISO codes of the ISO 3166 international standard\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-countrycodes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-countrycodes-syntax.json"></a>

```
{
  "[CountryCodes](#cfn-wafv2-rulegroup-countrycodes-countrycodes)" : [ [String](#aws-properties-wafv2-rulegroup-countrycodes), ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-countrycodes-syntax.yaml"></a>

```
  [CountryCodes](#cfn-wafv2-rulegroup-countrycodes-countrycodes): 
    - [String](#aws-properties-wafv2-rulegroup-countrycodes)
```

## Properties<a name="aws-properties-wafv2-rulegroup-countrycodes-properties"></a>

`CountryCodes`  <a name="cfn-wafv2-rulegroup-countrycodes-countrycodes"></a>
An array of two\-character country codes, for example, \[ "US", "CN" \], from the alpha\-2 country ISO codes of the ISO 3166 international standard\.   
*Required*: No  
*Type*: [List](#aws-properties-wafv2-rulegroup-countrycodes) of [String](#aws-properties-wafv2-rulegroup-countrycodes)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)