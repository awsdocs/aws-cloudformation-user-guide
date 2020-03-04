# AWS::WAFv2::RegexPatternSet Regex<a name="aws-properties-wafv2-regexpatternset-regex"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

A single regular expression\. This is used in a RegexPatternSet\.

## Syntax<a name="aws-properties-wafv2-regexpatternset-regex-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-regexpatternset-regex-syntax.json"></a>

```
{
  "[RegexString](#cfn-wafv2-regexpatternset-regex-regexstring)" : String
}
```

### YAML<a name="aws-properties-wafv2-regexpatternset-regex-syntax.yaml"></a>

```
  [RegexString](#cfn-wafv2-regexpatternset-regex-regexstring): 
    String
```

## Properties<a name="aws-properties-wafv2-regexpatternset-regex-properties"></a>

`RegexString`  <a name="cfn-wafv2-regexpatternset-regex-regexstring"></a>
The string representing the regular expression\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)