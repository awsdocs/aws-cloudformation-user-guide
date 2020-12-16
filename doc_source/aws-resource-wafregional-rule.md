# AWS::WAFRegional::Rule<a name="aws-resource-wafregional-rule"></a>

A combination of `ByteMatchSet`, `IPSet`, and/or `SqlInjectionMatchSet` objects that identify the web requests that you want to allow, block, or count\. For example, you might create a `Rule` that includes the following predicates:
+ An `IPSet` that causes AWS WAF to search for web requests that originate from the IP address `192.0.2.44` 
+ A `ByteMatchSet` that causes AWS WAF to search for web requests for which the value of the `User-Agent` header is `BadBot`\.

To match the settings in this `Rule`, a request must originate from `192.0.2.44` AND include a `User-Agent` header for which the value is `BadBot`\.

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
Type: AWS::WAFRegional::Rule
Properties: 
  [MetricName](#cfn-wafregional-rule-metricname): String
  [Name](#cfn-wafregional-rule-name): String
  [Predicates](#cfn-wafregional-rule-predicates): 
    - Predicate
```

## Properties<a name="aws-resource-wafregional-rule-properties"></a>

`MetricName`  <a name="cfn-wafregional-rule-metricname"></a>
A friendly name or description for the metrics for this `Rule`\. The name can contain only alphanumeric characters \(A\-Z, a\-z, 0\-9\), with maximum length 128 and minimum length one\. It can't contain whitespace or metric names reserved for AWS WAF, including "All" and "Default\_Action\." You can't change `MetricName` after you create the `Rule`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-wafregional-rule-name"></a>
The friendly name or description for the `Rule`\. You can't change the name of a `Rule` after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Predicates`  <a name="cfn-wafregional-rule-predicates"></a>
The `Predicates` object contains one `Predicate` element for each `ByteMatchSet`, `IPSet`, or `SqlInjectionMatchSet` object that you want to include in a `Rule`\.  
*Required*: No  
*Type*: List of [Predicate](aws-properties-wafregional-rule-predicate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafregional-rule-return-values"></a>

### Ref<a name="aws-resource-wafregional-rule-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-wafregional-rule--examples"></a>



### Associate an IPSet with a Web ACL Rule<a name="aws-resource-wafregional-rule--examples--Associate_an_IPSet_with_a_Web_ACL_Rule"></a>

The following example associates the `MyIPSetBlacklist` `IPSet` object with a web ACL rule\.

#### JSON<a name="aws-resource-wafregional-rule--examples--Associate_an_IPSet_with_a_Web_ACL_Rule--json"></a>

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

#### YAML<a name="aws-resource-wafregional-rule--examples--Associate_an_IPSet_with_a_Web_ACL_Rule--yaml"></a>

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