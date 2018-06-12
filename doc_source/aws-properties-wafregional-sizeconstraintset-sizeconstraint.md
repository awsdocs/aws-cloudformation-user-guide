# AWS WAF Regional SizeConstraintSet SizeConstraint<a name="aws-properties-wafregional-sizeconstraintset-sizeconstraint"></a>

`SizeConstraint` is a property of the [AWS::WAFRegional::SizeConstraintSet](aws-resource-wafregional-sizeconstraintset.md) resource that specifies a size constraint and which part of a web request that you want AWS WAF to constrain\.

## Syntax<a name="w3ab2c21c14e2056b5"></a>

### JSON<a name="aws-properties-wafregional-sizeconstraintset-sizeconstraint-syntax.json"></a>

```
{
  "[ComparisonOperator](#cfn-wafregional-sizeconstraintset-sizeconstraint-comparisonoperator)" : String,
  "[FieldToMatch](#cfn-wafregional-sizeconstraintset-sizeconstraint-fieldtomatch)" : Field to match,
  "[Size](#cfn-wafregional-sizeconstraintset-sizeconstraint-size)" : String,
  "[TextTransformation](#cfn-wafregional-sizeconstraintset-sizeconstraint-texttransformation)" : String
}
```

### YAML<a name="aws-properties-wafregional-sizeconstraintset-sizeconstraint-syntax.yaml"></a>

```
[ComparisonOperator](#cfn-wafregional-sizeconstraintset-sizeconstraint-comparisonoperator): String
[FieldToMatch](#cfn-wafregional-sizeconstraintset-sizeconstraint-fieldtomatch):
  Field to match
[Size](#cfn-wafregional-sizeconstraintset-sizeconstraint-size): String
[TextTransformation](#cfn-wafregional-sizeconstraintset-sizeconstraint-texttransformation): String
```

## Properties<a name="w3ab2c21c14e2056b7"></a>

`ComparisonOperator`  <a name="cfn-wafregional-sizeconstraintset-sizeconstraint-comparisonoperator"></a>
The type of comparison that you want AWS WAF to perform\. AWS WAF uses this value in combination with the `Size` and `FieldToMatch` property values to check if the size constraint is a match\. For more information and valid values, see the `ComparisonOperator` content for the [SizeConstraint](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_SizeConstraint.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String

`FieldToMatch`  <a name="cfn-wafregional-sizeconstraintset-sizeconstraint-fieldtomatch"></a>
The part of a web request that you want AWS WAF to search, such as a specific header or a query string\.  
*Required*: Yes  
*Type*: [AWS WAF Regional SizeConstraintSet SizeConstraint FieldToMatch](aws-properties-wafregional-sizeconstraintset-sizeconstraint-fieldtomatch.md)

`Size`  <a name="cfn-wafregional-sizeconstraintset-sizeconstraint-size"></a>
The size in bytes that you want AWS WAF to compare against the size of the specified `FieldToMatch`\. AWS WAF uses `Size` in combination with the `ComparisonOperator` and `FieldToMatch` property values to check if the size constraint of a web request is a match\. For more information and valid values, see the `Size` content for the [SizeConstraint](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_SizeConstraint.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: Integer

`TextTransformation`  <a name="cfn-wafregional-sizeconstraintset-sizeconstraint-texttransformation"></a>
Specifies how AWS WAF processes the `FieldToMatch` property before inspecting a request for a match\. Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass AWS WAF\. If you specify a transformation, AWS WAF transforms the `FieldToMatch` before inspecting a web request for a match\.  
For example, AWS WAF can replace white space characters \(such as `\t` and `\n`\) with a single space\. For valid values, see the `TextTransformation` content for the [SizeConstraint](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_SizeConstraint.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String