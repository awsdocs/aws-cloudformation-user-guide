# AWS::WAFv2::WebACL ManagedRuleGroupStatement<a name="aws-properties-wafv2-webacl-managedrulegroupstatement"></a>

A rule statement used to run the rules that are defined in a managed rule group\. To use this, provide the vendor name and the name of the rule group in this statement\. 

You can't nest a `ManagedRuleGroupStatement`, for example for use inside a `NotStatement` or `OrStatement`\. It can only be referenced as a top\-level statement within a rule\.

## Syntax<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-syntax.json"></a>

```
{
  "[ExcludedRules](#cfn-wafv2-webacl-managedrulegroupstatement-excludedrules)" : [ ExcludedRule, ... ],
  "[Name](#cfn-wafv2-webacl-managedrulegroupstatement-name)" : String,
  "[ScopeDownStatement](#cfn-wafv2-webacl-managedrulegroupstatement-scopedownstatement)" : Statement,
  "[VendorName](#cfn-wafv2-webacl-managedrulegroupstatement-vendorname)" : String,
  "[Version](#cfn-wafv2-webacl-managedrulegroupstatement-version)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-syntax.yaml"></a>

```
  [ExcludedRules](#cfn-wafv2-webacl-managedrulegroupstatement-excludedrules): 
    - ExcludedRule
  [Name](#cfn-wafv2-webacl-managedrulegroupstatement-name): String
  [ScopeDownStatement](#cfn-wafv2-webacl-managedrulegroupstatement-scopedownstatement): 
    Statement
  [VendorName](#cfn-wafv2-webacl-managedrulegroupstatement-vendorname): String
  [Version](#cfn-wafv2-webacl-managedrulegroupstatement-version): String
```

## Properties<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-properties"></a>

`ExcludedRules`  <a name="cfn-wafv2-webacl-managedrulegroupstatement-excludedrules"></a>
The rules whose actions are set to `COUNT` by the web ACL, regardless of the action that is configured in the rule\. This effectively excludes the rule from acting on web requests\.   
*Required*: No  
*Type*: List of [ExcludedRule](aws-properties-wafv2-webacl-excludedrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-webacl-managedrulegroupstatement-name"></a>
The name of the managed rule group\. You use this, along with the vendor name, to identify the rule group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScopeDownStatement`  <a name="cfn-wafv2-webacl-managedrulegroupstatement-scopedownstatement"></a>
Statement nested inside a managed rule group statement to narrow the scope of the requests that AWS WAF evaluates using the rule group\. Requests that match the scope\-down statement are evaluated using the rule group\. Requests that don't match the scope\-down statement are not a match for the managed rule group statement, without any further evaluation\.   
*Required*: No  
*Type*: [Statement](aws-properties-wafv2-webacl-statement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VendorName`  <a name="cfn-wafv2-webacl-managedrulegroupstatement-vendorname"></a>
The name of the managed rule group vendor\. You use this, along with the rule group name, to identify the rule group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-wafv2-webacl-managedrulegroupstatement-version"></a>
The version of the managed rule group to use\. Leave this empty to use the vendor's recommended version\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[\w#:\.\-/]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)