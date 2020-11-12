# AWS::WAFv2::WebACL ManagedRuleGroupStatement<a name="aws-properties-wafv2-webacl-managedrulegroupstatement"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

A rule statement used to run the rules that are defined in a managed rule group\. To use this, provide the vendor name and the name of the rule group in this statement\. You can retrieve the required names by calling ListAvailableManagedRuleGroups\.

You can't nest a `ManagedRuleGroupStatement`, for example for use inside a `NotStatement` or `OrStatement`\. It can only be referenced as a top\-level statement within a rule\.

## Syntax<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-syntax.json"></a>

```
{
  "[ExcludedRules](#cfn-wafv2-webacl-managedrulegroupstatement-excludedrules)" : [ ExcludedRule, ... ],
  "[Name](#cfn-wafv2-webacl-managedrulegroupstatement-name)" : String,
  "[VendorName](#cfn-wafv2-webacl-managedrulegroupstatement-vendorname)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-syntax.yaml"></a>

```
  [ExcludedRules](#cfn-wafv2-webacl-managedrulegroupstatement-excludedrules): 
    - ExcludedRule
  [Name](#cfn-wafv2-webacl-managedrulegroupstatement-name): String
  [VendorName](#cfn-wafv2-webacl-managedrulegroupstatement-vendorname): String
```

## Properties<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-properties"></a>

`ExcludedRules`  <a name="cfn-wafv2-webacl-managedrulegroupstatement-excludedrules"></a>
The rules whose actions are set to `COUNT` by the web ACL, regardless of the action that is set on the rule\. This effectively excludes the rule from acting on web requests\.   
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

`VendorName`  <a name="cfn-wafv2-webacl-managedrulegroupstatement-vendorname"></a>
The name of the managed rule group vendor\. You use this, along with the rule group name, to identify the rule group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)