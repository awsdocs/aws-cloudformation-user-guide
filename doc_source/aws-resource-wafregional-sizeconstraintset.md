# AWS::WAFRegional::SizeConstraintSet<a name="aws-resource-wafregional-sizeconstraintset"></a>

A complex type that contains `SizeConstraint` objects, which specify the parts of web requests that you want AWS WAF to inspect the size of\. If a `SizeConstraintSet` contains more than one `SizeConstraint` object, a request only needs to match one constraint to be considered a match\.

## Syntax<a name="aws-resource-wafregional-sizeconstraintset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-sizeconstraintset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::SizeConstraintSet",
  "Properties" : {
      "[Name](#cfn-wafregional-sizeconstraintset-name)" : String,
      "[SizeConstraints](#cfn-wafregional-sizeconstraintset-sizeconstraints)" : [ [SizeConstraint](aws-properties-wafregional-sizeconstraintset-sizeconstraint.md), ... ]
    }
}
```

### YAML<a name="aws-resource-wafregional-sizeconstraintset-syntax.yaml"></a>

```
Type: AWS::WAFRegional::SizeConstraintSet
Properties: 
  [Name](#cfn-wafregional-sizeconstraintset-name): String
  [SizeConstraints](#cfn-wafregional-sizeconstraintset-sizeconstraints): 
    - [SizeConstraint](aws-properties-wafregional-sizeconstraintset-sizeconstraint.md)
```

## Properties<a name="aws-resource-wafregional-sizeconstraintset-properties"></a>

`Name`  <a name="cfn-wafregional-sizeconstraintset-name"></a>
The name, if any, of the `SizeConstraintSet`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SizeConstraints`  <a name="cfn-wafregional-sizeconstraintset-sizeconstraints"></a>
The size constraint and the part of the web request to check\.  
*Required*: No  
*Type*: List of [SizeConstraint](aws-properties-wafregional-sizeconstraintset-sizeconstraint.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-wafregional-sizeconstraintset-return-values"></a>

### Ref<a name="aws-resource-wafregional-sizeconstraintset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-wafregional-sizeconstraintset--examples"></a>

### Define a Size Constraint<a name="aws-resource-wafregional-sizeconstraintset--examples--Define_a_Size_Constraint"></a>

The following example checks that the body of an HTTP request equals `4096` bytes\.

#### JSON<a name="aws-resource-wafregional-sizeconstraintset--examples--Define_a_Size_Constraint--json"></a>

```
"MySizeConstraint": {
  "Type": "AWS::WAFRegional::SizeConstraintSet",
  "Properties": {
    "Name": "SizeConstraints",
    "SizeConstraints": [
      {
        "ComparisonOperator": "EQ",
        "FieldToMatch": {
          "Type": "BODY"
        },
        "Size": "4096",
        "TextTransformation": "NONE"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-sizeconstraintset--examples--Define_a_Size_Constraint--yaml"></a>

```
  MySizeConstraint: 
    Type: "AWS::WAFRegional::SizeConstraintSet"
    Properties: 
      Name: "SizeConstraints"
      SizeConstraints: 
        - 
          ComparisonOperator: "EQ"
          FieldToMatch: 
            Type: "BODY"
          Size: "4096"
TextTransformation: "NONE"
```

### Associate a SizeConstraintSet with a Web ACL Rule<a name="aws-resource-wafregional-sizeconstraintset--examples--Associate_a_SizeConstraintSet_with_a_Web_ACL_Rule"></a>

The following example associates the `MySizeConstraint` object with a web ACL rule\.

#### JSON<a name="aws-resource-wafregional-sizeconstraintset--examples--Associate_a_SizeConstraintSet_with_a_Web_ACL_Rule--json"></a>

```
"SizeConstraintRule" : {
  "Type": "AWS::WAFRegional::Rule",
  "Properties": {
    "Name": "SizeConstraintRule",
    "MetricName" : "SizeConstraintRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "MySizeConstraint" },
        "Negated" : false,
        "Type" : "SizeConstraint"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-sizeconstraintset--examples--Associate_a_SizeConstraintSet_with_a_Web_ACL_Rule--yaml"></a>

```
SizeConstraintRule: 
  Type: "AWS::WAFRegional::Rule"
  Properties: 
    Name: "SizeConstraintRule"
    MetricName: "SizeConstraintRule"
    Predicates: 
      - 
        DataId: 
          Ref: "MySizeConstraint"
        Negated: false
Type: "SizeConstraint"
```

### Create a Web ACL<a name="aws-resource-wafregional-sizeconstraintset--examples--Create_a_Web_ACL"></a>

The following example associates the `SizeConstraintRule` rule with a web ACL\. The web ACL blocks all requests except for requests with a body size equal to `4096` bytes\.

#### JSON<a name="aws-resource-wafregional-sizeconstraintset--examples--Create_a_Web_ACL--json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
  "Properties": {
    "Name": "Web ACL to allow requests with a specific size",
    "DefaultAction": {
      "Type": "BLOCK"
    },
    "MetricName" : "SizeConstraintWebACL",
    "Rules": [
      {
        "Action" : {
          "Type" : "ALLOW"
        },
        "Priority" : 1,
        "RuleId" : { "Ref" : "SizeConstraintRule" }
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-wafregional-sizeconstraintset--examples--Create_a_Web_ACL--yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
  Properties: 
    Name: "Web ACL to allow requests with a specific size"
    DefaultAction: 
      Type: "BLOCK"
    MetricName: "SizeConstraintWebACL"
    Rules: 
      - 
        Action: 
          Type: "ALLOW"
        Priority: 1
        RuleId: 
Ref: "SizeConstraintRule"
```

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
