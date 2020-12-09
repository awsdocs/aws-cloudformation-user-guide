# AWS::WAFv2::WebACL OverrideAction<a name="aws-properties-wafv2-webacl-overrideaction"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

The action to use to override the `Action` settings on the rules in the web ACL\. You can use none, in which case the rule actions are in effect, or count, in which case, if a rule matches a web request, it only counts the match\.

## Syntax<a name="aws-properties-wafv2-webacl-overrideaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-overrideaction-syntax.json"></a>

```
{
  "[Count](#cfn-wafv2-webacl-overrideaction-count)" : Json,
  "[None](#cfn-wafv2-webacl-overrideaction-none)" : Json
}
```

### YAML<a name="aws-properties-wafv2-webacl-overrideaction-syntax.yaml"></a>

```
  [Count](#cfn-wafv2-webacl-overrideaction-count): Json
  [None](#cfn-wafv2-webacl-overrideaction-none): Json
```

## Properties<a name="aws-properties-wafv2-webacl-overrideaction-properties"></a>

`Count`  <a name="cfn-wafv2-webacl-overrideaction-count"></a>
Override the rule action settings to count\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`None`  <a name="cfn-wafv2-webacl-overrideaction-none"></a>
Don't override the rule action settings\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)