# AWS::WAF::SqlInjectionMatchSet<a name="aws-resource-waf-sqlinjectionmatchset"></a>

The `AWS::WAF::SqlInjectionMatchSet` resource creates an AWS WAF `SqlInjectionMatchSet`, which you use to allow, block, or count requests that contain malicious SQL code in a specific part of web requests\. For more information, see [CreateSqlInjectionMatchSet](http://docs.aws.amazon.com/waf/latest/APIReference/API_CreateSqlInjectionMatchSet.html) in the *AWS WAF API Reference*\.

**Topics**
+ [Syntax](#aws-resource-waf-sqlinjectionmatchset-syntax)
+ [Properties](#w3ab2c21c10e1201b9)
+ [Return Values](#w3ab2c21c10e1201c11)
+ [Examples](#w3ab2c21c10e1201c13)

## Syntax<a name="aws-resource-waf-sqlinjectionmatchset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-waf-sqlinjectionmatchset-syntax.json"></a>

```
{
  "Type" : "AWS::WAF::SqlInjectionMatchSet",
  "Properties" : {
    "[Name](#cfn-waf-sqlinjectionmatchset-name)" : String,
    "[SqlInjectionMatchTuples](#cfn-waf-sqlinjectionmatchset-sqlinjectionmatchtuples)" : [ SqlInjectionMatchTuple, ... ]
  }
}
```

### YAML<a name="aws-resource-waf-sqlinjectionmatchset-syntax.yaml"></a>

```
Type: "AWS::WAF::SqlInjectionMatchSet"
Properties: 
  [Name](#cfn-waf-sqlinjectionmatchset-name): String
  [SqlInjectionMatchTuples](#cfn-waf-sqlinjectionmatchset-sqlinjectionmatchtuples):
    - SqlInjectionMatchTuple
```

## Properties<a name="w3ab2c21c10e1201b9"></a>

`Name`  <a name="cfn-waf-sqlinjectionmatchset-name"></a>
A friendly name or description of the `SqlInjectionMatchSet`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SqlInjectionMatchTuples`  <a name="cfn-waf-sqlinjectionmatchset-sqlinjectionmatchtuples"></a>
The parts of web requests that you want AWS WAF to inspect for malicious SQL code and, if you want AWS WAF to inspect a header, the name of the header\.  
*Required*: No  
*Type*: List of [AWS WAF SqlInjectionMatchSet SqlInjectionMatchTuples](aws-properties-waf-sqlinjectionmatchset-sqlinjectionmatchtuples.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10e1201c11"></a>

### Ref<a name="w3ab2c21c10e1201c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource physical ID, such as `1234a1a-a1b1-12a1-abcd-a123b123456`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10e1201c13"></a>

### Find SQL Injections<a name="w3ab2c21c10e1201c13b2"></a>

The following example looks for snippets of SQL code in the query string of an HTTP request\.

#### JSON<a name="aws-resource-waf-sqlinjectionmatchset-example1.json"></a>

```
"SqlInjDetection": {
  "Type": "AWS::WAF::SqlInjectionMatchSet",
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

#### YAML<a name="aws-resource-waf-sqlinjectionmatchset-example1.yaml"></a>

```
SqlInjDetection: 
  Type: "AWS::WAF::SqlInjectionMatchSet"
  Properties: 
    Name: "Find SQL injections in the query string"
    SqlInjectionMatchTuples: 
      - 
        FieldToMatch: 
          Type: "QUERY_STRING"
        TextTransformation: "URL_DECODE"
```

### Associate a SQL Injection Match Set with a Web ACL Rule<a name="w3ab2c21c10e1201c13b4"></a>

The following example associates the `SqlInjDetection` match set with a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-waf-sqlinjectionmatchset-example2.json"></a>

```
"SqlInjRule" : {
  "Type": "AWS::WAF::Rule",
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

#### YAML<a name="aws-resource-waf-sqlinjectionmatchset-example2.yaml"></a>

```
SqlInjRule: 
  Type: "AWS::WAF::Rule"
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

### Create a Web ACL<a name="w3ab2c21c10e1201c13b6"></a>

The following example associates the `SqlInjRule` rule with a web ACL\. The web ACL allows all requests except for ones with SQL code in the query string of a request\.

#### JSON<a name="aws-resource-waf-sqlinjectionmatchset-example3.json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAF::WebACL",
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

#### YAML<a name="aws-resource-waf-sqlinjectionmatchset-example3.yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAF::WebACL"
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