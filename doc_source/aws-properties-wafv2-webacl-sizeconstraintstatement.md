# AWS::WAFv2::WebACL SizeConstraintStatement<a name="aws-properties-wafv2-webacl-sizeconstraintstatement"></a>

A rule statement that compares a number of bytes against the size of a request component, using a comparison operator, such as greater than \(>\) or less than \(<\)\. For example, you can use a size constraint statement to look for query strings that are longer than 100 bytes\. 

If you configure AWS WAF to inspect the request body, AWS WAF inspects only the first 8192 bytes \(8 KB\)\. If the request body for your web requests never exceeds 8192 bytes, you could use a size constraint statement to block requests that have a request body greater than 8192 bytes\.

If you choose URI for the value of Part of the request to filter on, the slash \(/\) in the URI counts as one character\. For example, the URI `/logo.jpg` is nine characters long\.

## Syntax<a name="aws-properties-wafv2-webacl-sizeconstraintstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-sizeconstraintstatement-syntax.json"></a>

```
{
  "[ComparisonOperator](#cfn-wafv2-webacl-sizeconstraintstatement-comparisonoperator)" : String,
  "[FieldToMatch](#cfn-wafv2-webacl-sizeconstraintstatement-fieldtomatch)" : FieldToMatch,
  "[Size](#cfn-wafv2-webacl-sizeconstraintstatement-size)" : Double,
  "[TextTransformations](#cfn-wafv2-webacl-sizeconstraintstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-sizeconstraintstatement-syntax.yaml"></a>

```
  [ComparisonOperator](#cfn-wafv2-webacl-sizeconstraintstatement-comparisonoperator): String
  [FieldToMatch](#cfn-wafv2-webacl-sizeconstraintstatement-fieldtomatch): 
    FieldToMatch
  [Size](#cfn-wafv2-webacl-sizeconstraintstatement-size): Double
  [TextTransformations](#cfn-wafv2-webacl-sizeconstraintstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-webacl-sizeconstraintstatement-properties"></a>

`ComparisonOperator`  <a name="cfn-wafv2-webacl-sizeconstraintstatement-comparisonoperator"></a>
The operator to use to compare the request part to the size setting\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `EQ | GE | GT | LE | LT | NE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldToMatch`  <a name="cfn-wafv2-webacl-sizeconstraintstatement-fieldtomatch"></a>
The part of the web request that you want AWS WAF to inspect\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-webacl-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-wafv2-webacl-sizeconstraintstatement-size"></a>
The size, in byte, to compare to the request part, after any transformations\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-webacl-sizeconstraintstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. If you specify one or more transformations in a rule statement, AWS WAF performs all transformations on the content of the request component identified by `FieldToMatch`, starting from the lowest priority setting, before inspecting the content for a match\.  
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)