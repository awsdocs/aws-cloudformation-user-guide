# AWS::WAFv2::WebACL OverrideAction<a name="aws-properties-wafv2-webacl-overrideaction"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

The action to use to override the rule's `Action` setting\. You can use no override action, in which case the rule action is in effect, or count, in which case, if the rule matches a web request, it only counts the match\.

## Syntax<a name="aws-properties-wafv2-webacl-overrideaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-overrideaction-syntax.json"></a>

```
{
  "[Count](#cfn-wafv2-webacl-overrideaction-count)" : [CountAction](aws-properties-wafv2-webacl-countaction.md),
  "[None](#cfn-wafv2-webacl-overrideaction-none)" : [NoneAction](aws-properties-wafv2-webacl-noneaction.md)
}
```

### YAML<a name="aws-properties-wafv2-webacl-overrideaction-syntax.yaml"></a>

```
  [Count](#cfn-wafv2-webacl-overrideaction-count): 
    [CountAction](aws-properties-wafv2-webacl-countaction.md)
  [None](#cfn-wafv2-webacl-overrideaction-none): 
    [NoneAction](aws-properties-wafv2-webacl-noneaction.md)
```

## Properties<a name="aws-properties-wafv2-webacl-overrideaction-properties"></a>

`Count`  <a name="cfn-wafv2-webacl-overrideaction-count"></a>
Override the rule action setting to count\.  
*Required*: No  
*Type*: [CountAction](aws-properties-wafv2-webacl-countaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`None`  <a name="cfn-wafv2-webacl-overrideaction-none"></a>
Don't override the rule action setting\.  
*Required*: No  
*Type*: [NoneAction](aws-properties-wafv2-webacl-noneaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)