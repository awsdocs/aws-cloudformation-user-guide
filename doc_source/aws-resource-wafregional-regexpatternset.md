# AWS::WAFRegional::RegexPatternSet<a name="aws-resource-wafregional-regexpatternset"></a>

The `RegexPatternSet` specifies the regular expression \(regex\) pattern that you want AWS WAF to search for, such as `B[a@]dB[o0]t`\. You can then configure AWS WAF to reject those requests\.

Note that you can only create regex pattern sets using a CloudFormation template\. To add the regex pattern sets created through CloudFormation to a RegexMatchSet, use the AWS WAF console, API, or command line interface \(CLI\)\. For more information, see [UpdateRegexMatchSet](https://docs.aws.amazon.com/waf/latest/APIReference/API_regional_UpdateRegexMatchSet.html)\.

## Syntax<a name="aws-resource-wafregional-regexpatternset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-regexpatternset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::RegexPatternSet",
  "Properties" : {
      "[Name](#cfn-wafregional-regexpatternset-name)" : String,
      "[RegexPatternStrings](#cfn-wafregional-regexpatternset-regexpatternstrings)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-wafregional-regexpatternset-syntax.yaml"></a>

```
Type: AWS::WAFRegional::RegexPatternSet
Properties: 
  [Name](#cfn-wafregional-regexpatternset-name): String
  [RegexPatternStrings](#cfn-wafregional-regexpatternset-regexpatternstrings): 
    - String
```

## Properties<a name="aws-resource-wafregional-regexpatternset-properties"></a>

`Name`  <a name="cfn-wafregional-regexpatternset-name"></a>
A friendly name or description of the [AWS::WAFRegional::RegexPatternSet](#aws-resource-wafregional-regexpatternset)\. You can't change `Name` after you create a `RegexPatternSet`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RegexPatternStrings`  <a name="cfn-wafregional-regexpatternset-regexpatternstrings"></a>
Specifies the regular expression \(regex\) patterns that you want AWS WAF to search for, such as `B[a@]dB[o0]t`\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafregional-regexpatternset-return-values"></a>

### Ref<a name="aws-resource-wafregional-regexpatternset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-wafregional-regexpatternset--examples"></a>



### Define Regular Expression Pattern<a name="aws-resource-wafregional-regexpatternset--examples--Define_Regular_Expression_Pattern"></a>

The following example defines a regular expression \(regex\) pattern for a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-wafregional-regexpatternset--examples--Define_Regular_Expression_Pattern--json"></a>

```
"MyRegexPatternSet": {
  "Type": "AWS::WAFRegional::RegexPatternSet",
  "Properties": {
    "Name": "Regex Pattern Set",
    "RegexPatternStrings": ["badbot", "danger"]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-regexpatternset--examples--Define_Regular_Expression_Pattern--yaml"></a>

```
MyRegexPatternSet: 
  Type: "AWS::WAFRegional::RegexPatternSet"
  Properties: 
    Name: "Regex Pattern Set"
    RegexPatternStrings: 
      - 
        "[B[a@]dB[o0]t"
      - 
        "D[a@]ng[e3]rStr[i1]ng"
```

### Associate a RegexPatternSet with a Web ACL Rule<a name="aws-resource-wafregional-regexpatternset--examples--Associate_a_RegexPatternSet_with_a_Web_ACL_Rule"></a>

The following example associates the `MyRegexPatternSet` with a web ACL rule\.

#### JSON<a name="aws-resource-wafregional-regexpatternset--examples--Associate_a_RegexPatternSet_with_a_Web_ACL_Rule--json"></a>

```
"MyRegexRule" : {
  "Type": "AWS::WAFRegional::Rule",
  "Properties": {
    "Name": "MyRegexRule",
    "MetricName" : "MyRegexRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "MyRegexPatternSet" },
        "Negated" : false,
        "Type" : "RegexMatch"
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-regexpatternset--examples--Associate_a_RegexPatternSet_with_a_Web_ACL_Rule--yaml"></a>

```
MyRegexRule: 
  Type: "AWS::WAFRegional::Rule"
  Properties: 
    Name: "MyRegexRule"
    MetricName: "MyRegexRule"
    Predicates: 
      - 
        DataId: 
          Ref: "MyRegexPatternSet"
        Negated: false
        Type: "RegexMatch"
```

### Create a Web ACL<a name="aws-resource-wafregional-regexpatternset--examples--Create_a_Web_ACL"></a>

The following example associates the `MyRegexRule` rule with a web ACL\. The web ACL allows requests except for those that include strings defined by `MyRegexRule`\.

#### JSON<a name="aws-resource-wafregional-regexpatternset--examples--Create_a_Web_ACL--json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
  "Properties": {
    "Name": "WebACL to block certain regex strings",
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
        "RuleId" : { "Ref" : "MyRegexRule" }
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-regexpatternset--examples--Create_a_Web_ACL--yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
  Properties: 
    Name: "WebACL to block certain regex strings"
    DefaultAction: 
      Type: "ALLOW"
    MetricName: "MyWebACL"
    Rules: 
      - 
        Action: 
          Type: "BLOCK"
        Priority: 1
        RuleId: 
          Ref: "MyRegexRule"
```