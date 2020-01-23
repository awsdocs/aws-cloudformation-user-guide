# AWS::WAFv2::RegexPatternSet RegularExpressionList<a name="aws-properties-wafv2-regexpatternset-regularexpressionlist"></a>

Array of regular expressions\. 

## Syntax<a name="aws-properties-wafv2-regexpatternset-regularexpressionlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-regexpatternset-regularexpressionlist-syntax.json"></a>

```
{
  "[RegularExpressionList](#cfn-wafv2-regexpatternset-regularexpressionlist-regularexpressionlist)" : [ [Regex](aws-properties-wafv2-regexpatternset-regex.md), ... ]
}
```

### YAML<a name="aws-properties-wafv2-regexpatternset-regularexpressionlist-syntax.yaml"></a>

```
  [RegularExpressionList](#cfn-wafv2-regexpatternset-regularexpressionlist-regularexpressionlist): 
    - [Regex](aws-properties-wafv2-regexpatternset-regex.md)
```

## Properties<a name="aws-properties-wafv2-regexpatternset-regularexpressionlist-properties"></a>

`RegularExpressionList`  <a name="cfn-wafv2-regexpatternset-regularexpressionlist-regularexpressionlist"></a>
Array of regular expressions\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-regexpatternset-regularexpressionlist) of [Regex](aws-properties-wafv2-regexpatternset-regex.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)