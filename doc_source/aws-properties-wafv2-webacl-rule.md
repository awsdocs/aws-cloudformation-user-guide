# AWS::WAFv2::WebACL Rule<a name="aws-properties-wafv2-webacl-rule"></a>

A single rule, which you can use in a [AWS::WAFv2::WebACL](aws-resource-wafv2-webacl.md) or [AWS::WAFv2::RuleGroup](aws-resource-wafv2-rulegroup.md) to identify web requests that you want to allow, block, or count\. Each rule includes one top\-level [Statement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-rule.html#cfn-wafv2-webacl-rule-statement) that AWS WAF uses to identify matching web requests, and parameters that govern how AWS WAF handles them\. 

## Syntax<a name="aws-properties-wafv2-webacl-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-rule-syntax.json"></a>

```
{
  "[Action](#cfn-wafv2-webacl-rule-action)" : RuleAction,
  "[CaptchaConfig](#cfn-wafv2-webacl-rule-captchaconfig)" : CaptchaConfig,
  "[ChallengeConfig](#cfn-wafv2-webacl-rule-challengeconfig)" : ChallengeConfig,
  "[Name](#cfn-wafv2-webacl-rule-name)" : String,
  "[OverrideAction](#cfn-wafv2-webacl-rule-overrideaction)" : OverrideAction,
  "[Priority](#cfn-wafv2-webacl-rule-priority)" : Integer,
  "[RuleLabels](#cfn-wafv2-webacl-rule-rulelabels)" : [ Label, ... ],
  "[Statement](#cfn-wafv2-webacl-rule-statement)" : Statement,
  "[VisibilityConfig](#cfn-wafv2-webacl-rule-visibilityconfig)" : VisibilityConfig
}
```

### YAML<a name="aws-properties-wafv2-webacl-rule-syntax.yaml"></a>

```
  [Action](#cfn-wafv2-webacl-rule-action): 
    RuleAction
  [CaptchaConfig](#cfn-wafv2-webacl-rule-captchaconfig): 
    CaptchaConfig
  [ChallengeConfig](#cfn-wafv2-webacl-rule-challengeconfig): 
    ChallengeConfig
  [Name](#cfn-wafv2-webacl-rule-name): String
  [OverrideAction](#cfn-wafv2-webacl-rule-overrideaction): 
    OverrideAction
  [Priority](#cfn-wafv2-webacl-rule-priority): Integer
  [RuleLabels](#cfn-wafv2-webacl-rule-rulelabels): 
    - Label
  [Statement](#cfn-wafv2-webacl-rule-statement): 
    Statement
  [VisibilityConfig](#cfn-wafv2-webacl-rule-visibilityconfig): 
    VisibilityConfig
```

## Properties<a name="aws-properties-wafv2-webacl-rule-properties"></a>

`Action`  <a name="cfn-wafv2-webacl-rule-action"></a>
The action that AWS WAF should take on a web request when it matches the rule's statement\. Settings at the web ACL level can override the rule action setting\.   
This is used only for rules whose statements don't reference a rule group\. Rule statements that reference a rule group are `RuleGroupReferenceStatement` and `ManagedRuleGroupStatement`\.   
You must set either this `Action` setting or the rule's `OverrideAction`, but not both:  
+ If the rule statement doesn't reference a rule group, you must set this rule action setting and you must not set the rule's override action setting\. 
+ If the rule statement references a rule group, you must not set this action setting, because the actions are already set on the rules inside the rule group\. You must set the rule's override action setting to indicate specifically whether to override the actions that are set on the rules in the rule group\. 
*Required*: Conditional  
*Type*: [RuleAction](aws-properties-wafv2-webacl-ruleaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaptchaConfig`  <a name="cfn-wafv2-webacl-rule-captchaconfig"></a>
Specifies how AWS WAF should handle `CAPTCHA` evaluations\. If you don't specify this, AWS WAF uses the `CAPTCHA` configuration that's defined for the web ACL\.   
*Required*: No  
*Type*: [CaptchaConfig](aws-properties-wafv2-webacl-captchaconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChallengeConfig`  <a name="cfn-wafv2-webacl-rule-challengeconfig"></a>
Specifies how AWS WAF should handle `Challenge` evaluations\. If you don't specify this, AWS WAF uses the challenge configuration that's defined for the web ACL\.   
*Required*: No  
*Type*: [ChallengeConfig](aws-properties-wafv2-webacl-challengeconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-webacl-rule-name"></a>
The name of the rule\. You can't change the name of a `Rule` after you create it\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OverrideAction`  <a name="cfn-wafv2-webacl-rule-overrideaction"></a>
The override action to apply to the rules in a rule group, instead of the individual rule action settings\. This is used only for rules whose statements reference a rule group\. Rule statements that reference a rule group are `RuleGroupReferenceStatement` and `ManagedRuleGroupStatement`\.   
Set the override action to none to leave the rule group rule actions in effect\. Set it to count to only count matches, regardless of the rule action settings\.   
You must set either this `OverrideAction` setting or the `Action` setting, but not both:   
+ If the rule statement references a rule group, you must set this override action setting and you must not set the rule's action setting\. 
+ If the rule statement doesn't reference a rule group, you must set the rule action setting and you must not set the rule's override action setting\. 
*Required*: Conditional  
*Type*: [OverrideAction](aws-properties-wafv2-webacl-overrideaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-wafv2-webacl-rule-priority"></a>
If you define more than one `Rule` in a `WebACL`, AWS WAF evaluates each request against the `Rules` in order based on the value of `Priority`\. AWS WAF processes rules with lower priority first\. The priorities don't need to be consecutive, but they must all be different\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleLabels`  <a name="cfn-wafv2-webacl-rule-rulelabels"></a>
Labels to apply to web requests that match the rule match statement\. AWS WAF applies fully qualified labels to matching web requests\. A fully qualified label is the concatenation of a label namespace and a rule label\. The rule's rule group or web ACL defines the label namespace\.   
Rules that run after this rule in the web ACL can match against these labels using a `LabelMatchStatement`\.  
For each label, provide a case\-sensitive string containing optional namespaces and a label name, according to the following guidelines:  
+ Separate each component of the label with a colon\. 
+ Each namespace or name can have up to 128 characters\.
+ You can specify up to 5 namespaces in a label\.
+ Don't use the following reserved words in your label specification: `aws`, `waf`, `managed`, `rulegroup`, `webacl`, `regexpatternset`, or `ipset`\.
For example, `myLabelName` or `nameSpace1:nameSpace2:myLabelName`\.   
*Required*: No  
*Type*: List of [Label](aws-properties-wafv2-webacl-label.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statement`  <a name="cfn-wafv2-webacl-rule-statement"></a>
The AWS WAF processing statement for the rule, for example [ByteMatchStatement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-statement.html#cfn-wafv2-rulegroup-statement-bytematchstatement) or [SizeConstraintStatement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-statement.html#cfn-wafv2-rulegroup-statement-sizeconstraintstatement)\.   
*Required*: Yes  
*Type*: [Statement](aws-properties-wafv2-webacl-statement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisibilityConfig`  <a name="cfn-wafv2-webacl-rule-visibilityconfig"></a>
Defines and enables Amazon CloudWatch metrics and web request sample collection\.   
*Required*: Yes  
*Type*: [VisibilityConfig](aws-properties-wafv2-webacl-visibilityconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)