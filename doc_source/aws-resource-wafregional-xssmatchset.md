# AWS::WAFRegional::XssMatchSet<a name="aws-resource-wafregional-xssmatchset"></a>

**Note**  
This is **AWS WAF Classic** documentation\. For more information, see [AWS WAF Classic](https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html) in the developer guide\.  
 **For the latest version of AWS WAF**, use the AWS WAFV2 API and see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. With the latest version, AWS WAF has a single set of endpoints for regional and global use\. 

A complex type that contains `XssMatchTuple` objects, which specify the parts of web requests that you want AWS WAF to inspect for cross\-site scripting attacks and, if you want AWS WAF to inspect a header, the name of the header\. If a `XssMatchSet` contains more than one `XssMatchTuple` object, a request needs to include cross\-site scripting attacks in only one of the specified parts of the request to be considered a match\.

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
Type: AWS::WAFRegional::XssMatchSet
Properties: 
  [Name](#cfn-wafregional-xssmatchset-name): String
  [XssMatchTuples](#cfn-wafregional-xssmatchset-xssmatchtuples): 
    - XssMatchTuple
```

## Properties<a name="aws-resource-wafregional-xssmatchset-properties"></a>

`Name`  <a name="cfn-wafregional-xssmatchset-name"></a>
The name, if any, of the `XssMatchSet`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`XssMatchTuples`  <a name="cfn-wafregional-xssmatchset-xssmatchtuples"></a>
Specifies the parts of web requests that you want to inspect for cross\-site scripting attacks\.  
*Required*: No  
*Type*: List of [XssMatchTuple](aws-properties-wafregional-xssmatchset-xssmatchtuple.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafregional-xssmatchset-return-values"></a>

### Ref<a name="aws-resource-wafregional-xssmatchset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-wafregional-xssmatchset--examples"></a>



### Define Which Part of a Request to Check for Cross\-site Scripting<a name="aws-resource-wafregional-xssmatchset--examples--Define_Which_Part_of_a_Request_to_Check_for_Cross-site_Scripting"></a>

The following example looks for cross\-site scripting in the URI or query string of an HTTP request\.

#### JSON<a name="aws-resource-wafregional-xssmatchset--examples--Define_Which_Part_of_a_Request_to_Check_for_Cross-site_Scripting--json"></a>

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

#### YAML<a name="aws-resource-wafregional-xssmatchset--examples--Define_Which_Part_of_a_Request_to_Check_for_Cross-site_Scripting--yaml"></a>

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

### Associate an XssMatchSet with a Web ACL Rule<a name="aws-resource-wafregional-xssmatchset--examples--Associate_an_XssMatchSet_with_a_Web_ACL_Rule"></a>

The following example associates the `DetectXSS` match set with a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-wafregional-xssmatchset--examples--Associate_an_XssMatchSet_with_a_Web_ACL_Rule--json"></a>

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

#### YAML<a name="aws-resource-wafregional-xssmatchset--examples--Associate_an_XssMatchSet_with_a_Web_ACL_Rule--yaml"></a>

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

### Create a Web ACL<a name="aws-resource-wafregional-xssmatchset--examples--Create_a_Web_ACL"></a>

The following example associates the `XSSRule` rule with a web ACL\. The web ACL allows all requests except for ones that contain cross\-site scripting in the URI or query string of an HTTP request\.

#### JSON<a name="aws-resource-wafregional-xssmatchset--examples--Create_a_Web_ACL--json"></a>

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

#### YAML<a name="aws-resource-wafregional-xssmatchset--examples--Create_a_Web_ACL--yaml"></a>

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