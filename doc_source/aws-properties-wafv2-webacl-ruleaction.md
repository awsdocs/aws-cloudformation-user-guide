# AWS::WAFv2::WebACL RuleAction<a name="aws-properties-wafv2-webacl-ruleaction"></a>

The action that AWS WAF should take on a web request when it matches a rule's statement\. Settings at the web ACL level can override the rule action setting\. 

## Syntax<a name="aws-properties-wafv2-webacl-ruleaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ruleaction-syntax.json"></a>

```
{
  "[Allow](#cfn-wafv2-webacl-ruleaction-allow)" : AllowAction,
  "[Block](#cfn-wafv2-webacl-ruleaction-block)" : BlockAction,
  "[Count](#cfn-wafv2-webacl-ruleaction-count)" : CountAction
}
```

### YAML<a name="aws-properties-wafv2-webacl-ruleaction-syntax.yaml"></a>

```
  [Allow](#cfn-wafv2-webacl-ruleaction-allow): 
    AllowAction
  [Block](#cfn-wafv2-webacl-ruleaction-block): 
    BlockAction
  [Count](#cfn-wafv2-webacl-ruleaction-count): 
    CountAction
```

## Properties<a name="aws-properties-wafv2-webacl-ruleaction-properties"></a>

`Allow`  <a name="cfn-wafv2-webacl-ruleaction-allow"></a>
Instructs AWS WAF to allow the web request\.  
*Required*: No  
*Type*: [AllowAction](aws-properties-wafv2-webacl-allowaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Block`  <a name="cfn-wafv2-webacl-ruleaction-block"></a>
Instructs AWS WAF to block the web request\.  
*Required*: No  
*Type*: [BlockAction](aws-properties-wafv2-webacl-blockaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Count`  <a name="cfn-wafv2-webacl-ruleaction-count"></a>
Instructs AWS WAF to count the web request and allow it\.  
*Required*: No  
*Type*: [CountAction](aws-properties-wafv2-webacl-countaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)