# AWS::WAFv2::RuleGroup SizeConstraintStatement<a name="aws-properties-wafv2-rulegroup-sizeconstraintstatement"></a>

A rule statement that compares a number of bytes against the size of a request component, using a comparison operator, such as greater than \(>\) or less than \(<\)\. For example, you can use a size constraint statement to look for query strings that are longer than 100 bytes\. 

If you configure AWS WAF to inspect the request body, AWS WAF inspects only the number of bytes of the body up to the limit for the web ACL\. By default, for regional web ACLs, this limit is 8 KB \(8,192 kilobytes\) and for CloudFront web ACLs, this limit is 16 KB \(16,384 kilobytes\)\. For CloudFront web ACLs, you can increase the limit in the web ACL `AssociationConfig`, for additional fees\. If you know that the request body for your web requests should never exceed the inspection limit, you could use a size constraint statement to block requests that have a larger request body size\.

If you choose URI for the value of Part of the request to filter on, the slash \(/\) in the URI counts as one character\. For example, the URI `/logo.jpg` is nine characters long\.

## Syntax<a name="aws-properties-wafv2-rulegroup-sizeconstraintstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-sizeconstraintstatement-syntax.json"></a>

```
{
  "[ComparisonOperator](#cfn-wafv2-rulegroup-sizeconstraintstatement-comparisonoperator)" : String,
  "[FieldToMatch](#cfn-wafv2-rulegroup-sizeconstraintstatement-fieldtomatch)" : FieldToMatch,
  "[Size](#cfn-wafv2-rulegroup-sizeconstraintstatement-size)" : Double,
  "[TextTransformations](#cfn-wafv2-rulegroup-sizeconstraintstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-sizeconstraintstatement-syntax.yaml"></a>

```
  [ComparisonOperator](#cfn-wafv2-rulegroup-sizeconstraintstatement-comparisonoperator): String
  [FieldToMatch](#cfn-wafv2-rulegroup-sizeconstraintstatement-fieldtomatch): 
    FieldToMatch
  [Size](#cfn-wafv2-rulegroup-sizeconstraintstatement-size): Double
  [TextTransformations](#cfn-wafv2-rulegroup-sizeconstraintstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-rulegroup-sizeconstraintstatement-properties"></a>

`ComparisonOperator`  <a name="cfn-wafv2-rulegroup-sizeconstraintstatement-comparisonoperator"></a>
The operator to use to compare the request part to the size setting\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `EQ | GE | GT | LE | LT | NE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldToMatch`  <a name="cfn-wafv2-rulegroup-sizeconstraintstatement-fieldtomatch"></a>
The part of the web request that you want AWS WAF to inspect\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-rulegroup-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-wafv2-rulegroup-sizeconstraintstatement-size"></a>
The size, in byte, to compare to the request part, after any transformations\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-rulegroup-sizeconstraintstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. Text transformations are used in rule match statements, to transform the `FieldToMatch` request component before inspecting it, and they're used in rate\-based rule statements, to transform request components before using them as custom aggregation keys\. If you specify one or more transformations to apply, AWS WAF performs all transformations on the specified content, starting from the lowest priority setting, and then uses the component contents\.   
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-rulegroup-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)