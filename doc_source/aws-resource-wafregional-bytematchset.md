# AWS::WAFRegional::ByteMatchSet<a name="aws-resource-wafregional-bytematchset"></a>

The `AWS::WAFRegional::ByteMatchSet` resource creates an AWS WAF Regional `ByteMatchSet` that identifies a part of a web request that you want to inspect\. For more information, see [CreateByteMatchSet](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_CreateByteMatchSet.html) in the *AWS WAF Regional API Reference*\.

**Topics**
+ [Syntax](#aws-resource-wafregional-bytematchset-syntax)
+ [Properties](#w3ab2c21c10e1213b9)
+ [Return Values](#w3ab2c21c10e1213c11)
+ [Examples](#w3ab2c21c10e1213c13)

## Syntax<a name="aws-resource-wafregional-bytematchset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-bytematchset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::ByteMatchSet",
  "Properties" : {
    "[ByteMatchTuples](#cfn-wafregional-bytematchset-bytematchtuples)" : [ Byte match tuple, ... ],
    "[Name](#cfn-wafregional-bytematchset-name)" : String
  }
}
```

### YAML<a name="aws-resource-wafregional-bytematchset-syntax.yaml"></a>

```
Type: "AWS::WAFRegional::ByteMatchSet"
Properties: 
  [ByteMatchTuples](#cfn-wafregional-bytematchset-bytematchtuples):
    - Byte match tuple
  [Name](#cfn-wafregional-bytematchset-name): String
```

## Properties<a name="w3ab2c21c10e1213b9"></a>

`ByteMatchTuples`  <a name="cfn-wafregional-bytematchset-bytematchtuples"></a>
Settings for the `ByteMatchSet`, such as the bytes \(typically a string that corresponds with ASCII characters\) that you want AWS WAF to search for in web requests\.  
*Required*: No  
*Type*: List of [AWS WAF Regional ByteMatchSet ByteMatchTuples](aws-properties-wafregional-bytematchset-bytematchtuples.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-wafregional-bytematchset-name"></a>
A friendly name or description of the `ByteMatchSet`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10e1213c11"></a>

### Ref<a name="w3ab2c21c10e1213c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource physical ID, such as `1234a1a-a1b1-12a1-abcd-a123b123456`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10e1213c13"></a>

### HTTP Referers<a name="w3ab2c21c10e1213c13b2"></a>

The following example defines a set of HTTP referers to match\.

#### JSON<a name="aws-resource-wafregional-bytematchset-example.json"></a>

```
"BadReferers": {
  "Type": "AWS::WAFRegional::ByteMatchSet",
  "Properties": {
    "Name": "ByteMatch for matching bad HTTP referers",
    "ByteMatchTuples": [
      {
        "FieldToMatch" : {
          "Type": "HEADER",
          "Data": "referer"
        },
        "TargetString" : "badrefer1",
        "TextTransformation" : "NONE",
        "PositionalConstraint" : "CONTAINS"
      },
      {
        "FieldToMatch" : {
          "Type": "HEADER",
          "Data": "referer"
        },
        "TargetString" : "badrefer2",
        "TextTransformation" : "NONE",
        "PositionalConstraint" : "CONTAINS"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-bytematchset-example.yaml"></a>

```
BadReferers: 
  Type: "AWS::WAFRegional::ByteMatchSet"
  Properties: 
    Name: "ByteMatch for matching bad HTTP referers"
    ByteMatchTuples: 
      - 
        FieldToMatch: 
          Type: "HEADER"
          Data: "referer"
        TargetString: "badrefer1"
        TextTransformation: "NONE"
        PositionalConstraint: "CONTAINS"
      - 
        FieldToMatch: 
          Type: "HEADER"
          Data: "referer"
        TargetString: "badrefer2"
        TextTransformation: "NONE"
        PositionalConstraint: "CONTAINS"
```

### Associate a ByteMatchSet with a Web ACL Rule<a name="w3ab2c21c10e1213c13b4"></a>

The following example associates the `BadReferers` byte match set with a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-wafregional-bytematchset-example2.json"></a>

```
"BadReferersRule" : {
  "Type": "AWS::WAFRegional::Rule",
  "Properties": {
    "Name": "BadReferersRule",
    "MetricName" : "BadReferersRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "BadReferers" },
        "Negated" : false,
        "Type" : "ByteMatch"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-bytematchset-example2.yaml"></a>

```
BadReferersRule: 
  Type: "AWS::WAFRegional::Rule"
  Properties: 
    Name: "BadReferersRule"
    MetricName: "BadReferersRule"
    Predicates: 
      - 
        DataId: 
          Ref: "BadReferers"
        Negated: false
        Type: "ByteMatch"
```

### Create a Web ACL<a name="w3ab2c21c10e1213c13b6"></a>

The following example associates the `BadReferersRule` rule with a web ACL\. The web ACL allows all requests except for ones with referers that match the `BadReferersRule` rule\.

#### JSON<a name="aws-resource-wafregional-bytematchset-example3.json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
  "Properties": {
    "Name": "WebACL to block blacklisted IP addresses",
    "DefaultAction": {
      "Type": "ALLOW"
    },
    "MetricName" : "MyWebACL",
    "Rules": [
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 1,
        "RuleId" : { "Ref" : "BadReferersRule" }
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-bytematchset-example3.yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
  Properties: 
    Name: "WebACL to block blacklisted IP addresses"
    DefaultAction: 
      Type: "ALLOW"
    MetricName: "MyWebACL"
    Rules: 
      - 
        Action: 
          Type: "BLOCK"
        Priority: 1
        RuleId: 
          Ref: "BadReferersRule"
```