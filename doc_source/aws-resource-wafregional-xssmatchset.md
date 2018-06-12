# AWS::WAFRegional::XssMatchSet<a name="aws-resource-wafregional-xssmatchset"></a>

The `AWS::WAFRegional::XssMatchSet` resource specifies the parts of web requests that you want AWS WAF to inspect for cross\-site scripting attacks and the name of the header to inspect\. For more information, see [XssMatchSet](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_XssMatchSet.html) in the *AWS WAF Regional API Reference*\.

**Topics**
+ [Syntax](#aws-resource-wafregional-xssmatchset-syntax)
+ [Properties](#w3ab2c21c10e1241b9)
+ [Return Value](#w3ab2c21c10e1241c11)
+ [Examples](#w3ab2c21c10e1241c13)

## Syntax<a name="aws-resource-wafregional-xssmatchset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-xssmatchset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::XssMatchSet",
  "Properties" : {
    "[Name](#cfn-wafregional-xssmatchset-name)" : String,
    "[XssMatchTuples](#cfn-wafregional-xssmatchset-xssmatchtuples)" : [ XssMatchTuple, ... ]
  }
}
```

### YAML<a name="aws-resource-wafregional-xssmatchset-syntax.yaml"></a>

```
Type: "AWS::WAFRegional::XssMatchSet"
Properties: 
  [Name](#cfn-wafregional-xssmatchset-name): String
  [XssMatchTuples](#cfn-wafregional-xssmatchset-xssmatchtuples):
    - XssMatchTuple
```

## Properties<a name="w3ab2c21c10e1241b9"></a>

`Name`  <a name="cfn-wafregional-xssmatchset-name"></a>
A friendly name or description for the `XssMatchSet`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`XssMatchTuples`  <a name="cfn-wafregional-xssmatchset-xssmatchtuples"></a>
The parts of web requests that you want to inspect for cross\-site scripting attacks\.  
*Required*: No  
*Type*: List of [AWS WAF Regional XssMatchSet XssMatchTuple](aws-properties-wafregional-xssmatchset-xssmatchtuple.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10e1241c11"></a>

### Ref<a name="w3ab2c21c10e1241c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource physical ID, such as `1234a1a-a1b1-12a1-abcd-a123b123456`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10e1241c13"></a>

### Define Which Part of a Request to Check for Cross\-site Scripting<a name="w3ab2c21c10e1241c13b2"></a>

The following example looks for cross\-site scripting in the URI or query string of an HTTP request\.

#### JSON<a name="aws-resource-wafregional-xssmatchset-example1.json"></a>

```
"DetectXSS": {
  "Type": "AWS::WAFRegional::XssMatchSet",
  "Properties": {
    "Name": "XssMatchSet",
    "XssMatchTuples": [
      {
        "FieldToMatch": {
          "Type": "URI"
        },
        "TextTransformation": "NONE"
      },
      {
        "FieldToMatch": {
          "Type": "QUERY_STRING"
        },
        "TextTransformation": "NONE"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-xssmatchset-example1.yaml"></a>

```
DetectXSS: 
  Type: "AWS::WAFRegional::XssMatchSet"
  Properties: 
    Name: "XssMatchSet"
    XssMatchTuples: 
      - 
        FieldToMatch: 
          Type: "URI"
        TextTransformation: "NONE"
      - 
        FieldToMatch: 
          Type: "QUERY_STRING"
        TextTransformation: "NONE"
```

### Associate an XssMatchSet with a Web ACL Rule<a name="w3ab2c21c10e1241c13b4"></a>

The following example associates the `DetectXSS` match set with a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-wafregional-xssmatchset-example2.json"></a>

```
"XSSRule" : {
  "Type": "AWS::WAFRegional::Rule",
  "Properties": {
    "Name": "XSSRule",
    "MetricName" : "XSSRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "DetectXSS" },
        "Negated" : false,
        "Type" : "XssMatch"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-xssmatchset-example2.yaml"></a>

```
XSSRule: 
  Type: "AWS::WAFRegional::Rule"
  Properties: 
    Name: "XSSRule"
    MetricName: "XSSRule"
    Predicates: 
      - 
        DataId: 
          Ref: "DetectXSS"
        Negated: false
        Type: "XssMatch"
```

### Create a Web ACL<a name="w3ab2c21c10e1241c13b6"></a>

The following example associates the `XSSRule` rule with a web ACL\. The web ACL allows all requests except for ones that contain cross\-site scripting in the URI or query string of an HTTP request\.

#### JSON<a name="aws-resource-wafregional-xssmatchset-example3.json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
  "Properties": {
    "Name": "Web ACL to block cross-site scripting",
    "DefaultAction": {
      "Type": "ALLOW"
    },
    "MetricName" : "DetectXSSWebACL",
    "Rules": [
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 1,
        "RuleId" : { "Ref" : "XSSRule" }
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-xssmatchset-example3.yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
  Properties: 
    Name: "Web ACL to block cross-site scripting"
    DefaultAction: 
      Type: "ALLOW"
    MetricName: "DetectXSSWebACL"
    Rules: 
      - 
        Action: 
          Type: "BLOCK"
        Priority: 1
        RuleId: 
          Ref: "XSSRule"
```