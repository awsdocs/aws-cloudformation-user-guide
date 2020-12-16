# AWS::WAFv2::RuleGroup RuleAction<a name="aws-properties-wafv2-rulegroup-ruleaction"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

The action that AWS WAF should take on a web request when it matches a rule's statement\. Settings at the web ACL level can override the rule action setting\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-ruleaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-ruleaction-syntax.json"></a>

```
{
  "[Allow](#cfn-wafv2-rulegroup-ruleaction-allow)" : Json,
  "[Block](#cfn-wafv2-rulegroup-ruleaction-block)" : Json,
  "[Count](#cfn-wafv2-rulegroup-ruleaction-count)" : Json
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-ruleaction-syntax.yaml"></a>

```
  [Allow](#cfn-wafv2-rulegroup-ruleaction-allow): Json
  [Block](#cfn-wafv2-rulegroup-ruleaction-block): Json
  [Count](#cfn-wafv2-rulegroup-ruleaction-count): Json
```

## Properties<a name="aws-properties-wafv2-rulegroup-ruleaction-properties"></a>

`Allow`  <a name="cfn-wafv2-rulegroup-ruleaction-allow"></a>
Instructs AWS WAF to allow the web request\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Block`  <a name="cfn-wafv2-rulegroup-ruleaction-block"></a>
Instructs AWS WAF to block the web request\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Count`  <a name="cfn-wafv2-rulegroup-ruleaction-count"></a>
Instructs AWS WAF to count the web request and allow it\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)