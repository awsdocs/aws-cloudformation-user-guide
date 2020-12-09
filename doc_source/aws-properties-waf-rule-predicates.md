# AWS::WAF::Rule Predicate<a name="aws-properties-waf-rule-predicates"></a>

Specifies the `ByteMatchSet`, `IPSet`, `SqlInjectionMatchSet`, `XssMatchSet`, `RegexMatchSet`, `GeoMatchSet`, and `SizeConstraintSet` objects that you want to add to a `Rule` and, for each object, indicates whether you want to negate the settings, for example, requests that do NOT originate from the IP address 192\.0\.2\.44\. 

## Syntax<a name="aws-properties-waf-rule-predicates-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-waf-rule-predicates-properties"></a>

`DataId`  <a name="cfn-waf-rule-predicates-dataid"></a>
A unique identifier for a predicate in a `Rule`, such as `ByteMatchSetId` or `IPSetId`\. The ID is returned by the corresponding `Create` or `List` command\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Negated`  <a name="cfn-waf-rule-predicates-negated"></a>
Set `Negated` to `False` if you want AWS WAF to allow, block, or count requests based on the settings in the specified `ByteMatchSet`, `IPSet`, `SqlInjectionMatchSet`, `XssMatchSet`, `RegexMatchSet`, `GeoMatchSet`, or `SizeConstraintSet`\. For example, if an `IPSet` includes the IP address `192.0.2.44`, AWS WAF will allow or block requests based on that IP address\.  
Set `Negated` to `True` if you want AWS WAF to allow or block a request based on the negation of the settings in the `ByteMatchSet`, `IPSet`, `SqlInjectionMatchSet`, `XssMatchSet`, `RegexMatchSet`, `GeoMatchSet`, or `SizeConstraintSet`\. For example, if an `IPSet` includes the IP address `192.0.2.44`, AWS WAF will allow, block, or count requests based on all IP addresses *except* `192.0.2.44`\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-waf-rule-predicates-type"></a>
The type of predicate in a `Rule`, such as `ByteMatch` or `IPSet`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ByteMatch | GeoMatch | IPMatch | RegexMatch | SizeConstraint | SqlInjectionMatch | XssMatch`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)