# AWS::WAFRegional::Rule<a name="aws-resource-wafregional-rule"></a>

The `AWS::WAFRegional::Rule` resource creates an AWS WAF Regional rule that specifies a combination of `IPSet`, `ByteMatchSet`, and `SqlInjectionMatchSet` objects that identify the web requests to allow, block, or count\. To implement rules, you must associate them with a [web ACL](aws-resource-wafregional-webacl.md)\.

For more information, see [CreateRule](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_CreateRule.html) in the *AWS WAF Regional API Reference*\.

**Topics**
+ [Syntax](#aws-resource-wafregional-rule-syntax)
+ [Properties](#w3ab2c21c10e1221c11)
+ [Return Value](#w3ab2c21c10e1221c13)
+ [Example](#w3ab2c21c10e1221c15)

## Syntax<a name="aws-resource-wafregional-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-rule-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::Rule",
  "Properties" : {
    "[MetricName](#cfn-wafregional-rule-metricname)" : String,
    "[Name](#cfn-wafregional-rule-name)" : String,
    "[Predicates](#cfn-wafregional-rule-predicates)" : [ Predicate, ... ]
  }
}
```

### YAML<a name="aws-resource-wafregional-rule-syntax.yaml"></a>

```
Type: "AWS::WAFRegional::Rule"
Properties: 
  [MetricName](#cfn-wafregional-rule-metricname): String
  [Name](#cfn-wafregional-rule-name): String
  [Predicates](#cfn-wafregional-rule-predicates):
    - Predicate
```

## Properties<a name="w3ab2c21c10e1221c11"></a>

`MetricName`  <a name="cfn-wafregional-rule-metricname"></a>
A friendly name or description for the metrics of the rule\. For valid values, see the `MetricName` parameter for the [http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_CreateRule.html](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_CreateRule.html) action in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-wafregional-rule-name"></a>
A friendly name or description of the rule\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Predicates`  <a name="cfn-wafregional-rule-predicates"></a>
The `ByteMatchSet`, `IPSet`, `SizeConstraintSet`, `SqlInjectionMatchSet`, or `XssMatchSet` objects to include in a rule\. If you add more than one predicate to a rule, a request must match all conditions in order to be allowed or blocked\.  
*Required*: No  
*Type*: List of [AWS WAF Regional Rule Predicates](aws-properties-wafregional-rule-predicates.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10e1221c13"></a>

### Ref<a name="w3ab2c21c10e1221c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource physical ID, such as `1234a1a-a1b1-12a1-abcd-a123b123456`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10e1221c15"></a>

### Associate an IPSet with a Web ACL Rule<a name="w3ab2c21c10e1221c15b2"></a>

The following example associates the `MyIPSetBlacklist` `IPSet` object with a web ACL rule\.

#### JSON<a name="aws-resource-wafregional-rule-example.json"></a>

```
"MyIPSetRule" : {
  "Type": "AWS::WAFRegional::Rule",
  "Properties": {
    "Name": "MyIPSetRule",
    "MetricName" : "MyIPSetRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "MyIPSetBlacklist" },
        "Negated" : false,
        "Type" : "IPMatch"
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-rule-example.yaml"></a>

```
MyIPSetRule: 
  Type: "AWS::WAFRegional::Rule"
  Properties: 
    Name: "MyIPSetRule"
    MetricName: "MyIPSetRule"
    Predicates: 
      - 
        DataId: 
          Ref: "MyIPSetBlacklist"
        Negated: false
        Type: "IPMatch"
```