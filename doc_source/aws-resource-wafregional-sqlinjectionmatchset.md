# AWS::WAFRegional::SqlInjectionMatchSet<a name="aws-resource-wafregional-sqlinjectionmatchset"></a>

**Note**  
This is **AWS WAF Classic** documentation\. For more information, see [AWS WAF Classic](https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html) in the developer guide\.  
 **For the latest version of AWS WAF**, use the AWS WAFV2 API and see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. With the latest version, AWS WAF has a single set of endpoints for regional and global use\. 

A complex type that contains `SqlInjectionMatchTuple` objects, which specify the parts of web requests that you want AWS WAF to inspect for snippets of malicious SQL code and, if you want AWS WAF to inspect a header, the name of the header\. If a `SqlInjectionMatchSet` contains more than one `SqlInjectionMatchTuple` object, a request needs to include snippets of SQL code in only one of the specified parts of the request to be considered a match\.

## Syntax<a name="aws-resource-wafregional-sqlinjectionmatchset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-sqlinjectionmatchset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::SqlInjectionMatchSet",
  "Properties" : {
      "[Name](#cfn-wafregional-sqlinjectionmatchset-name)" : String,
      "[SqlInjectionMatchTuples](#cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples)" : [ SqlInjectionMatchTuple, ... ]
    }
}
```

### YAML<a name="aws-resource-wafregional-sqlinjectionmatchset-syntax.yaml"></a>

```
Type: AWS::WAFRegional::SqlInjectionMatchSet
Properties: 
  [Name](#cfn-wafregional-sqlinjectionmatchset-name): String
  [SqlInjectionMatchTuples](#cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples): 
    - SqlInjectionMatchTuple
```

## Properties<a name="aws-resource-wafregional-sqlinjectionmatchset-properties"></a>

`Name`  <a name="cfn-wafregional-sqlinjectionmatchset-name"></a>
The name, if any, of the `SqlInjectionMatchSet`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SqlInjectionMatchTuples`  <a name="cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples"></a>
Specifies the parts of web requests that you want to inspect for snippets of malicious SQL code\.  
*Required*: No  
*Type*: List of [SqlInjectionMatchTuple](aws-properties-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuple.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafregional-sqlinjectionmatchset-return-values"></a>

### Ref<a name="aws-resource-wafregional-sqlinjectionmatchset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-wafregional-sqlinjectionmatchset--examples"></a>



### Find SQL Injections<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Find_SQL_Injections"></a>

The following example looks for snippets of SQL code in the query string of an HTTP request\.

#### JSON<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Find_SQL_Injections--json"></a>

```
"SqlInjDetection": {
  "Type": "AWS::WAFRegional::SqlInjectionMatchSet",
  "Properties": {
    "Name": "Find SQL injections in the query string",
    "SqlInjectionMatchTuples": [
      {
        "FieldToMatch" : {
          "Type": "QUERY_STRING"
        },
        "TextTransformation" : "URL_DECODE"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Find_SQL_Injections--yaml"></a>

```
SqlInjDetection: 
  Type: "AWS::WAFRegional::SqlInjectionMatchSet"
  Properties: 
    Name: "Find SQL injections in the query string"
    SqlInjectionMatchTuples: 
      - 
        FieldToMatch: 
          Type: "QUERY_STRING"
        TextTransformation: "URL_DECODE"
```

### Associate a SQL Injection Match Set with a Web ACL Rule<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Associate_a_SQL_Injection_Match_Set_with_a_Web_ACL_Rule"></a>

The following example associates the `SqlInjDetection` match set with a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Associate_a_SQL_Injection_Match_Set_with_a_Web_ACL_Rule--json"></a>

```
"SqlInjRule" : {
  "Type": "AWS::WAFRegional::Rule",
  "Properties": {
    "Name": "SqlInjRule",
    "MetricName" : "SqlInjRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "SqlInjDetection" },
        "Negated" : false,
        "Type" : "SqlInjectionMatch"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Associate_a_SQL_Injection_Match_Set_with_a_Web_ACL_Rule--yaml"></a>

```
SqlInjRule: 
  Type: "AWS::WAFRegional::Rule"
  Properties: 
    Name: "SqlInjRule"
    MetricName: "SqlInjRule"
    Predicates: 
      - 
        DataId: 
          Ref: "SqlInjDetection"
        Negated: false
        Type: "SqlInjectionMatch"
```

### Create a Web ACL<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Create_a_Web_ACL"></a>

The following example associates the `SqlInjRule` rule with a web ACL\. The web ACL allows all requests except for ones with SQL code in the query string of a request\.

#### JSON<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Create_a_Web_ACL--json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
  "Properties": {
    "Name": "Web ACL to block SQL injection in the query string",
    "DefaultAction": {
      "Type": "ALLOW"
    },
    "MetricName" : "SqlInjWebACL",
    "Rules": [
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 1,
        "RuleId" : { "Ref" : "SqlInjRule" }
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-sqlinjectionmatchset--examples--Create_a_Web_ACL--yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
  Properties: 
    Name: "Web ACL to block SQL injection in the query string"
    DefaultAction: 
      Type: "ALLOW"
    MetricName: "SqlInjWebACL"
    Rules: 
      - 
        Action: 
          Type: "BLOCK"
        Priority: 1
        RuleId: 
          Ref: "SqlInjRule"
```