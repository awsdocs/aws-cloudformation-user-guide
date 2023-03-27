# AWS::WAFv2::RuleGroup LabelMatchStatement<a name="aws-properties-wafv2-rulegroup-labelmatchstatement"></a>

A rule statement to match against labels that have been added to the web request by rules that have already run in the web ACL\. 

The label match statement provides the label or namespace string to search for\. The label string can represent a part or all of the fully qualified label name that had been added to the web request\. Fully qualified labels have a prefix, optional namespaces, and label name\. The prefix identifies the rule group or web ACL context of the rule that added the label\. If you do not provide the fully qualified name in your label match string, AWS WAF performs the search for labels that were added in the same context as the label match statement\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-labelmatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-labelmatchstatement-syntax.json"></a>

```
{
  "[Key](#cfn-wafv2-rulegroup-labelmatchstatement-key)" : String,
  "[Scope](#cfn-wafv2-rulegroup-labelmatchstatement-scope)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-labelmatchstatement-syntax.yaml"></a>

```
  [Key](#cfn-wafv2-rulegroup-labelmatchstatement-key): String
  [Scope](#cfn-wafv2-rulegroup-labelmatchstatement-scope): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-labelmatchstatement-properties"></a>

`Key`  <a name="cfn-wafv2-rulegroup-labelmatchstatement-key"></a>
The string to match against\. The setting you provide for this depends on the match statement's `Scope` setting:   
+ If the `Scope` indicates `LABEL`, then this specification must include the name and can include any number of preceding namespace specifications and prefix up to providing the fully qualified label name\. 
+ If the `Scope` indicates `NAMESPACE`, then this specification can include any number of contiguous namespace strings, and can include the entire label namespace prefix from the rule group or web ACL where the label originates\.
Labels are case sensitive and components of a label must be separated by colon, for example `NS1:NS2:name`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^[0-9A-Za-z_\-:]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-wafv2-rulegroup-labelmatchstatement-scope"></a>
Specify whether you want to match using the label name or just the namespace\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `LABEL | NAMESPACE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)