# AWS::WAFv2::LoggingConfiguration ActionCondition<a name="aws-properties-wafv2-loggingconfiguration-actioncondition"></a>

A single action condition for a condition in a logging filter\.

## Syntax<a name="aws-properties-wafv2-loggingconfiguration-actioncondition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-loggingconfiguration-actioncondition-syntax.json"></a>

```
{
  "[Action](#cfn-wafv2-loggingconfiguration-actioncondition-action)" : String
}
```

### YAML<a name="aws-properties-wafv2-loggingconfiguration-actioncondition-syntax.yaml"></a>

```
  [Action](#cfn-wafv2-loggingconfiguration-actioncondition-action): String
```

## Properties<a name="aws-properties-wafv2-loggingconfiguration-actioncondition-properties"></a>

`Action`  <a name="cfn-wafv2-loggingconfiguration-actioncondition-action"></a>
The action setting that a log record must contain in order to meet the condition\. This is the action that AWS WAF applied to the web request\.   
For rule groups, this is either the configured rule action setting, or if you've applied a rule action override to the rule, it's the override action\. The value `EXCLUDED_AS_COUNT` matches on excluded rules and also on rules that have a rule action override of Count\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALLOW | BLOCK | CAPTCHA | CHALLENGE | COUNT | EXCLUDED_AS_COUNT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)