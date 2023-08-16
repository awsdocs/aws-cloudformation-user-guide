# AWS::WAFv2::RuleGroup RateLimitLabelNamespace<a name="aws-properties-wafv2-rulegroup-ratelimitlabelnamespace"></a>

Specifies a label namespace to use as an aggregate key for a rate\-based rule\. Each distinct fully qualified label name that has the specified label namespace contributes to the aggregation instance\. If you use just one label namespace as your custom key, then each label name fully defines an aggregation instance\. 

This uses only labels that have been added to the request by rules that are evaluated before this rate\-based rule in the web ACL\. 

For information about label namespaces and names, see [Label syntax and naming requirements](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-label-requirements.html) in the * AWS WAF Developer Guide*\.

## Syntax<a name="aws-properties-wafv2-rulegroup-ratelimitlabelnamespace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-ratelimitlabelnamespace-syntax.json"></a>

```
{
  "[Namespace](#cfn-wafv2-rulegroup-ratelimitlabelnamespace-namespace)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-ratelimitlabelnamespace-syntax.yaml"></a>

```
  [Namespace](#cfn-wafv2-rulegroup-ratelimitlabelnamespace-namespace): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-ratelimitlabelnamespace-properties"></a>

`Namespace`  <a name="cfn-wafv2-rulegroup-ratelimitlabelnamespace-namespace"></a>
The namespace to use for aggregation\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^[0-9A-Za-z_\-:]+:$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)