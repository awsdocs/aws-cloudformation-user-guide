# AWS WAF Regional Rule Predicates<a name="aws-properties-wafregional-rule-predicates"></a>

`Predicates` is a property of the [AWS::WAFRegional::Rule](aws-resource-wafregional-rule.md) resource that specifies the `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects to include in an AWS WAF Regional rule\. If you add more than one predicate to a rule, an incoming request must match all of the specifications in the predicates to be allowed or blocked\.

## Syntax<a name="w3ab2c21c14e2052b5"></a>

### JSON<a name="aws-properties-wafregional-rule-predicates-syntax.json"></a>

```
{
  "[DataId](#cfn-wafregional-rule-predicates-dataid)" : String,
  "[Negated](#cfn-wafregional-rule-predicates-negated)" : Boolean,
  "[Type](#cfn-wafregional-rule-predicates-type)" : String
}
```

### YAML<a name="aws-properties-wafregional-rule-predicates-syntax.yaml"></a>

```
[DataId](#cfn-wafregional-rule-predicates-dataid): String
[Negated](#cfn-wafregional-rule-predicates-negated): Boolean
[Type](#cfn-wafregional-rule-predicates-type): String
```

## Properties<a name="w3ab2c21c14e2052b7"></a>

`DataId`  <a name="cfn-wafregional-rule-predicates-dataid"></a>
The unique identifier of a predicate, such as the ID of a `ByteMatchSet` or `IPSet`\.  
*Required*: Yes  
*Type*: String

`Negated`  <a name="cfn-wafregional-rule-predicates-negated"></a>
Whether to use the settings or the negated settings that you specified in the `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects\.  
If you want AWS WAF to allow, block, or count requests based on the settings in the specified `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects, specify `false`\. For example, if an `IPSet` object includes the IP address `192.0.2.44`, AWS WAF allows, blocks, or counts requests originating from that IP address\.  
If you want AWS WAF to allow, block, or count requests based on the *negated* settings in the `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects, specify `true`\. For example, if an `IPSet` object includes the IP address `192.0.2.44`, AWS WAF allows, blocks, or counts requests originating from all IP addresses except 192\.0\.2\.44\.  
*Required*: Yes  
*Type*: Boolean

`Type`  <a name="cfn-wafregional-rule-predicates-type"></a>
The type of predicate in a rule, such as an `IPSet` \(`IPMatch`\)\. For valid values, see the `Type` contents of the [Predicate](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_Predicate.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String