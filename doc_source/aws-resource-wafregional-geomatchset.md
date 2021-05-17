# AWS::WAFRegional::GeoMatchSet<a name="aws-resource-wafregional-geomatchset"></a>

**Note**  
This is **AWS WAF Classic** documentation\. For more information, see [AWS WAF Classic](https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html) in the developer guide\.  
 **For the latest version of AWS WAF**, use the AWS WAFV2 API and see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. With the latest version, AWS WAF has a single set of endpoints for regional and global use\. 

Contains one or more countries that AWS WAF will search for\.

## Syntax<a name="aws-resource-wafregional-geomatchset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-geomatchset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::GeoMatchSet",
  "Properties" : {
      "[GeoMatchConstraints](#cfn-wafregional-geomatchset-geomatchconstraints)" : [ GeoMatchConstraint, ... ],
      "[Name](#cfn-wafregional-geomatchset-name)" : String
    }
}
```

### YAML<a name="aws-resource-wafregional-geomatchset-syntax.yaml"></a>

```
Type: AWS::WAFRegional::GeoMatchSet
Properties: 
  [GeoMatchConstraints](#cfn-wafregional-geomatchset-geomatchconstraints): 
    - GeoMatchConstraint
  [Name](#cfn-wafregional-geomatchset-name): String
```

## Properties<a name="aws-resource-wafregional-geomatchset-properties"></a>

`GeoMatchConstraints`  <a name="cfn-wafregional-geomatchset-geomatchconstraints"></a>
An array of `GeoMatchConstraint` objects, which contain the country that you want AWS WAF to search for\.  
*Required*: No  
*Type*: List of [GeoMatchConstraint](aws-properties-wafregional-geomatchset-geomatchconstraint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafregional-geomatchset-name"></a>
A friendly name or description of the [AWS::WAFRegional::GeoMatchSet](#aws-resource-wafregional-geomatchset)\. You can't change the name of an `GeoMatchSet` after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-wafregional-geomatchset-return-values"></a>

### Ref<a name="aws-resource-wafregional-geomatchset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-wafregional-geomatchset--examples"></a>



### Define Geographic Constraints<a name="aws-resource-wafregional-geomatchset--examples--Define_Geographic_Constraints"></a>

The following example defines a set of GeoMatchConstraints for a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-wafregional-geomatchset--examples--Define_Geographic_Constraints--json"></a>

```
"MyGeoConstraints": {
  "Type": "AWS::WAFRegional::GeoMatchSet",
  "Properties": {
    "Name": "GeoMatchSet for restricted countries",
    "GeoMatchConstraints": [
      {
        "Type" : "Country",
        "Value" : "AE"
      },
      {
        "Type" : "Country",
        "Value" : "ZW"
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-geomatchset--examples--Define_Geographic_Constraints--yaml"></a>

```
MyGeoConstraints: 
  Type: "AWS::WAFRegional::GeoMatchSet"
  Properties: 
    Name: "GeoMatchSet for restricted countries"
    GeoMatchConstraints: 
      - 
        Type: "Country"
        Value: "AE"
      - 
        Type: "Country"
        Value: "AE"
```

### Associate a GeoMatchSet with a Web ACL Rule<a name="aws-resource-wafregional-geomatchset--examples--Associate_a_GeoMatchSet_with_a_Web_ACL_Rule"></a>

The following example associates the `MyGeoConstraints` with a web ACL rule\.

#### JSON<a name="aws-resource-wafregional-geomatchset--examples--Associate_a_GeoMatchSet_with_a_Web_ACL_Rule--json"></a>

```
"MyGeoMatchRule" : {
  "Type": "AWS::WAFRegional::Rule",
  "Properties": {
    "Name": "MyGeoMatchRule",
    "MetricName" : "MyGeoMatchRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "MyGeoConstraints" },
        "Negated" : false,
        "Type" : "GeoMatch"
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-geomatchset--examples--Associate_a_GeoMatchSet_with_a_Web_ACL_Rule--yaml"></a>

```
MyGeoMatchRule: 
  Type: "AWS::WAFRegional::Rule"
  Properties: 
    Name: "MyGeoMatchRule"
    MetricName: "MyGeoMatchRule"
    Predicates: 
      - 
        DataId: 
          Ref: "MyGeoConstraints"
        Negated: false
        Type: "GeoMatch"
```

### Create a Web ACL<a name="aws-resource-wafregional-geomatchset--examples--Create_a_Web_ACL"></a>

The following example associates the `MyGeoMatchRule` rule with a web ACL\. The web ACL allows requests that originate from all countries except for those that are defined in the `MyGeoMatchRule`\.

#### JSON<a name="aws-resource-wafregional-geomatchset--examples--Create_a_Web_ACL--json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
  "Properties": {
    "Name": "WebACL to block restricted countries",
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
        "RuleId" : { "Ref" : "MyGeoMatchRule" }
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-geomatchset--examples--Create_a_Web_ACL--yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
  Properties: 
    Name: "WebACL to block restricted countries"
    DefaultAction: 
      Type: "ALLOW"
    MetricName: "MyWebACL"
    Rules: 
      - 
        Action: 
          Type: "BLOCK"
        Priority: 1
        RuleId: 
          Ref: "MyGeoMatchRule"
```