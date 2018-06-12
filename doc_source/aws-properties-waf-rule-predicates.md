# AWS WAF Rule Predicates<a name="aws-properties-waf-rule-predicates"></a>

`Predicates` is a property of the [AWS::WAF::Rule](aws-resource-waf-rule.md) resource that specifies the `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects to include in an AWS WAF rule\. If you add more than one predicate to a rule, an incoming request must match all of the specifications in the predicates to be allowed or blocked\.

## Syntax<a name="w3ab2c21c14e2003b5"></a>

### JSON<a name="aws-properties-waf-rule-predicates-syntax.json"></a>

```
{
  "[DataId](#cfn-waf-rule-predicates-dataid)" : String,
  "[Negated](#cfn-waf-rule-predicates-negated)" : Boolean,
  "[Type](#cfn-waf-rule-predicates-type)" : String
}
```

### YAML<a name="aws-properties-waf-rule-predicates-syntax.yaml"></a>

```
[DataId](#cfn-waf-rule-predicates-dataid): String
[Negated](#cfn-waf-rule-predicates-negated): Boolean
[Type](#cfn-waf-rule-predicates-type): String
```

## Properties<a name="w3ab2c21c14e2003b7"></a>

`DataId`  <a name="cfn-waf-rule-predicates-dataid"></a>
The unique identifier of a predicate, such as the ID of a `ByteMatchSet` or `IPSet`\.  
*Required*: Yes  
*Type*: String

`Negated`  <a name="cfn-waf-rule-predicates-negated"></a>
Whether to use the settings or the negated settings that you specified in the `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects\.  
Specify `false` if you want AWS WAF to allow, block, or count requests based on the settings in the specified `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects\. For example, if an `IPSet` object includes the IP address `192.0.2.44`, AWS WAF allows, blocks, or counts requests originating from that IP address\.  
Specify `true` if you want AWS WAF to allow, block, or count requests based on the negated settings in the `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects\. For example, if an `IPSet` object includes the IP address `192.0.2.44`, AWS WAF allows, blocks, or counts requests originating from all IP addresses except 192\.0\.2\.44\.  
*Required*: Yes  
*Type*: Boolean

`Type`  <a name="cfn-waf-rule-predicates-type"></a>
The type of predicate in a rule, such as an `IPSet` \(`IPMatch`\)\. For valid values, see the `Type` contents of the [Predicate](http://docs.aws.amazon.com/waf/latest/APIReference/API_Predicate.html) data type in the *AWS WAF API Reference*\.  
*Required*: Yes  
*Type*: String