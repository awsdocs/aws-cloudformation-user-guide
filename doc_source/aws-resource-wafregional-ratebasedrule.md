# AWS::WAFRegional::RateBasedRule<a name="aws-resource-wafregional-ratebasedrule"></a>

A `RateBasedRule` is identical to a regular `Rule`, with one addition: a `RateBasedRule` counts the number of requests that arrive from a specified IP address every five minutes\. For example, based on recent requests that you've seen from an attacker, you might create a `RateBasedRule` that includes the following conditions: 
+ The requests come from 192\.0\.2\.44\.
+ They contain the value `BadBot` in the `User-Agent` header\.

In the rule, you also define the rate limit as 15,000\.

Requests that meet both of these conditions and exceed 15,000 requests every five minutes trigger the rule's action \(block or count\), which is defined in the web ACL\.

Note you can only create rate\-based rules using a CloudFormation template\. To add the rate\-based rules created through CloudFormation to a web ACL, use the AWS WAF console, API, or command line interface \(CLI\)\. For more information, see [UpdateWebACL](https://docs.aws.amazon.com/waf/latest/APIReference/API_regional_UpdateWebACL.html)\.

## Syntax<a name="aws-resource-wafregional-ratebasedrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-ratebasedrule-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::RateBasedRule",
  "Properties" : {
      "[MatchPredicates](#cfn-wafregional-ratebasedrule-matchpredicates)" : [ Predicate, ... ],
      "[MetricName](#cfn-wafregional-ratebasedrule-metricname)" : String,
      "[Name](#cfn-wafregional-ratebasedrule-name)" : String,
      "[RateKey](#cfn-wafregional-ratebasedrule-ratekey)" : String,
      "[RateLimit](#cfn-wafregional-ratebasedrule-ratelimit)" : Integer
    }
}
```

### YAML<a name="aws-resource-wafregional-ratebasedrule-syntax.yaml"></a>

```
Type: AWS::WAFRegional::RateBasedRule
Properties: 
  [MatchPredicates](#cfn-wafregional-ratebasedrule-matchpredicates): 
    - Predicate
  [MetricName](#cfn-wafregional-ratebasedrule-metricname): String
  [Name](#cfn-wafregional-ratebasedrule-name): String
  [RateKey](#cfn-wafregional-ratebasedrule-ratekey): String
  [RateLimit](#cfn-wafregional-ratebasedrule-ratelimit): Integer
```

## Properties<a name="aws-resource-wafregional-ratebasedrule-properties"></a>

`MatchPredicates`  <a name="cfn-wafregional-ratebasedrule-matchpredicates"></a>
The `Predicates` object contains one `Predicate` element for each `ByteMatchSet`, `IPSet`, or `SqlInjectionMatchSet>` object that you want to include in a `RateBasedRule`\.  
*Required*: No  
*Type*: List of [Predicate](aws-properties-wafregional-ratebasedrule-predicate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-wafregional-ratebasedrule-metricname"></a>
A friendly name or description for the metrics for a `RateBasedRule`\. The name can contain only alphanumeric characters \(A\-Z, a\-z, 0\-9\), with maximum length 128 and minimum length one\. It can't contain whitespace or metric names reserved for AWS WAF, including "All" and "Default\_Action\." You can't change the name of the metric after you create the `RateBasedRule`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-wafregional-ratebasedrule-name"></a>
A friendly name or description for a `RateBasedRule`\. You can't change the name of a `RateBasedRule` after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RateKey`  <a name="cfn-wafregional-ratebasedrule-ratekey"></a>
The field that AWS WAF uses to determine if requests are likely arriving from single source and thus subject to rate monitoring\. The only valid value for `RateKey` is `IP`\. `IP` indicates that requests arriving from the same IP address are subject to the `RateLimit` that is specified in the `RateBasedRule`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `IP`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RateLimit`  <a name="cfn-wafregional-ratebasedrule-ratelimit"></a>
The maximum number of requests, which have an identical value in the field specified by the `RateKey`, allowed in a five\-minute period\. If the number of requests exceeds the `RateLimit` and the other predicates specified in the rule are also met, AWS WAF triggers the action that is specified for this rule\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafregional-ratebasedrule-return-values"></a>

### Ref<a name="aws-resource-wafregional-ratebasedrule-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-wafregional-ratebasedrule--examples"></a>



### Associate an IPSet with a Rate\-Based Rule<a name="aws-resource-wafregional-ratebasedrule--examples--Associate_an_IPSet_with_a_Rate-Based_Rule"></a>

The following example associates the `MyIPSetBlacklist` `IPSet` object with a rate\-based rule\.

#### JSON<a name="aws-resource-wafregional-ratebasedrule--examples--Associate_an_IPSet_with_a_Rate-Based_Rule--json"></a>

```
"MyIPSetRateBasedRule" : {
  "Type": "AWS::WAFRegional::RateBasedRule",
  "Properties": {
    "Name": "MyIPSetRateBasedRule",
    "MetricName" : "MyIPSetRateBasedRule",
    "RateKey" : "IP",
    "RateLimit" : 8000
    "MatchPredicates": [
      {
        "DataId" : {  "Ref" : "MyIPSetBlacklist" },
        "Negated" : false,
        "Type" : "IPMatch"
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-ratebasedrule--examples--Associate_an_IPSet_with_a_Rate-Based_Rule--yaml"></a>

```
MyIPSetRateBasedRule: 
  Type: "AWS::WAFRegional::RateBasedRule"
  Properties: 
    Name: "MyIPSetRateBasedRule"
    MetricName: "MyIPSetRateBasedRule"
    RateKey : "IP"
    RateLimit : 8000
    MatchPredicates: 
      - 
        DataId: 
          Ref: "MyIPSetBlacklist"
        Negated: false
        Type: "IPMatch"
```