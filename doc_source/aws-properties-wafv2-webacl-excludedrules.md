# AWS::WAFv2::WebACL ExcludedRules<a name="aws-properties-wafv2-webacl-excludedrules"></a>

Rules to exclude from rule processing\.

## Syntax<a name="aws-properties-wafv2-webacl-excludedrules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-excludedrules-syntax.json"></a>

```
{
  "[ExcludedRules](#cfn-wafv2-webacl-excludedrules-excludedrules)" : [ [ExcludedRule](aws-properties-wafv2-webacl-excludedrule.md), ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-excludedrules-syntax.yaml"></a>

```
  [ExcludedRules](#cfn-wafv2-webacl-excludedrules-excludedrules): 
    - [ExcludedRule](aws-properties-wafv2-webacl-excludedrule.md)
```

## Properties<a name="aws-properties-wafv2-webacl-excludedrules-properties"></a>

`ExcludedRules`  <a name="cfn-wafv2-webacl-excludedrules-excludedrules"></a>
Rules to exclude from rule processing\.  
*Required*: No  
*Type*: [List](#aws-properties-wafv2-webacl-excludedrules) of [ExcludedRule](aws-properties-wafv2-webacl-excludedrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)