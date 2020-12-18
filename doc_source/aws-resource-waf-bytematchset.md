# AWS::WAF::ByteMatchSet<a name="aws-resource-waf-bytematchset"></a>

The `AWS::WAF::ByteMatchSet` resource creates an AWS WAF `ByteMatchSet` that identifies a part of a web request that you want to inspect\.

## Syntax<a name="aws-resource-waf-bytematchset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-waf-bytematchset-syntax.json"></a>

```
{
  "Type" : "AWS::WAF::ByteMatchSet",
  "Properties" : {
      "[ByteMatchTuples](#cfn-waf-bytematchset-bytematchtuples)" : [ ByteMatchTuple, ... ],
      "[Name](#cfn-waf-bytematchset-name)" : String
    }
}
```

### YAML<a name="aws-resource-waf-bytematchset-syntax.yaml"></a>

```
Type: AWS::WAF::ByteMatchSet
Properties: 
  [ByteMatchTuples](#cfn-waf-bytematchset-bytematchtuples): 
    - ByteMatchTuple
  [Name](#cfn-waf-bytematchset-name): String
```

## Properties<a name="aws-resource-waf-bytematchset-properties"></a>

`ByteMatchTuples`  <a name="cfn-waf-bytematchset-bytematchtuples"></a>
Specifies the bytes \(typically a string that corresponds with ASCII characters\) that you want AWS WAF to search for in web requests, the location in requests that you want AWS WAF to search, and other settings\.  
*Required*: No  
*Type*: List of [ByteMatchTuple](aws-properties-waf-bytematchset-bytematchtuples.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-waf-bytematchset-name"></a>
A friendly name or description of the `ByteMatchSet`\. You can't change `Name` after you create a `ByteMatchSet`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-waf-bytematchset-return-values"></a>

### Ref<a name="aws-resource-waf-bytematchset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-waf-bytematchset--examples"></a>



### HTTP Referers<a name="aws-resource-waf-bytematchset--examples--HTTP_Referers"></a>

The following example defines a set of HTTP referers to match\.

#### JSON<a name="aws-resource-waf-bytematchset--examples--HTTP_Referers--json"></a>

```
"BadReferers": {
  "Type": "AWS::WAF::ByteMatchSet",
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

#### YAML<a name="aws-resource-waf-bytematchset--examples--HTTP_Referers--yaml"></a>

```
BadReferers: 
  Type: "AWS::WAF::ByteMatchSet"
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

### Associate a ByteMatchSet with a Web ACL Rule<a name="aws-resource-waf-bytematchset--examples--Associate_a_ByteMatchSet_with_a_Web_ACL_Rule"></a>

The following example associates the `BadReferers` byte match set with a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-waf-bytematchset--examples--Associate_a_ByteMatchSet_with_a_Web_ACL_Rule--json"></a>

```
"BadReferersRule" : {
  "Type": "AWS::WAF::Rule",
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

#### YAML<a name="aws-resource-waf-bytematchset--examples--Associate_a_ByteMatchSet_with_a_Web_ACL_Rule--yaml"></a>

```
BadReferersRule: 
  Type: "AWS::WAF::Rule"
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

### Create a Web ACL<a name="aws-resource-waf-bytematchset--examples--Create_a_Web_ACL"></a>

The following example associates the `BadReferersRule` rule with a web ACL\. The web ACL allows all requests except for ones with referers that match the `BadReferersRule` rule\.

#### JSON<a name="aws-resource-waf-bytematchset--examples--Create_a_Web_ACL--json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAF::WebACL",
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

#### YAML<a name="aws-resource-waf-bytematchset--examples--Create_a_Web_ACL--yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAF::WebACL"
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