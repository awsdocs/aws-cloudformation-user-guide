# AWS::WAFv2::WebACL ExcludedRule<a name="aws-properties-wafv2-webacl-excludedrule"></a>

Specifies a single rule to exclude from the rule group\. Excluding a rule overrides its action setting for the rule group in the web ACL, setting it to `COUNT`\. This effectively excludes the rule from acting on web requests\. 

## Syntax<a name="aws-properties-wafv2-webacl-excludedrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-excludedrule-syntax.json"></a>

```
{
  "[Name](#cfn-wafv2-webacl-excludedrule-name)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-excludedrule-syntax.yaml"></a>

```
  [Name](#cfn-wafv2-webacl-excludedrule-name): String
```

## Properties<a name="aws-properties-wafv2-webacl-excludedrule-properties"></a>

`Name`  <a name="cfn-wafv2-webacl-excludedrule-name"></a>
The name of the rule to exclude\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)