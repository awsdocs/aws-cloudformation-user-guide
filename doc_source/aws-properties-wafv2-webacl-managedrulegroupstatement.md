# AWS::WAFv2::WebACL ManagedRuleGroupStatement<a name="aws-properties-wafv2-webacl-managedrulegroupstatement"></a>

A rule statement used to run the rules that are defined in a managed rule group\. To use this, provide the vendor name and the name of the rule group in this statement\. 

You can't nest a `ManagedRuleGroupStatement`, for example for use inside a `NotStatement` or `OrStatement`\. It can only be referenced as a top\-level statement within a rule\.

## Syntax<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-managedrulegroupstatement-syntax.json"></a>

```
{
  "[ExcludedRules](#cfn-wafv2-webacl-managedrulegroupstatement-excludedrules)" : [ ExcludedRule, ... ],
  "[ManagedRuleGroupConfigs](#cfn-wafv2-webacl-managedrulegroupstatement-managedrulegroupconfigs)" : [ ManagedRuleGroupConfig, ... ],
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
  [ManagedRuleGroupConfigs](#cfn-wafv2-webacl-managedrulegroupstatement-managedrulegroupconfigs): 
    - ManagedRuleGroupConfig
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
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedRuleGroupConfigs`  <a name="cfn-wafv2-webacl-managedrulegroupstatement-managedrulegroupconfigs"></a>
Additional information that's used by a managed rule group\. Most managed rule groups don't require this\.  
Use this for the account takeover prevention managed rule group `AWSManagedRulesATPRuleSet`, to provide information about the sign\-in page of your application\.   
You can provide multiple individual `ManagedRuleGroupConfig` objects for any rule group configuration, for example `UsernameField` and `PasswordField`\. The configuration that you provide depends on the needs of the managed rule group\. For the ATP managed rule group, you provide the following individual configuration objects: `LoginPath`, `PasswordField`, `PayloadType` and `UsernameField`\.  
*Required*: No  
*Type*: List of [ManagedRuleGroupConfig](aws-properties-wafv2-webacl-managedrulegroupconfig.md)  
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
The version of the managed rule group to use\. If you specify this, the version setting is fixed until you change it\. If you don't specify this, AWS WAF uses the vendor's default version, and then keeps the version at the vendor's default when the vendor updates the managed rule group settings\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-managedrulegroupstatement--examples"></a>



### Configure the managed rule group statement for `AWSManagedRulesATPRuleSet`<a name="aws-properties-wafv2-webacl-managedrulegroupstatement--examples--Configure_the_managed_rule_group_statement_for_AWSManagedRulesATPRuleSet_"></a>

The following shows an example `ManagedRuleGroupStatement` for the AWS WAF ATP managed rule group\. The `ManagedRuleGroupConfigs` settings are provided as a number of individual `ManagedRuleGroupConfig` settings\.

#### YAML<a name="aws-properties-wafv2-webacl-managedrulegroupstatement--examples--Configure_the_managed_rule_group_statement_for_AWSManagedRulesATPRuleSet_--yaml"></a>

```
ManagedRuleGroupStatement:
  VendorName: AWS
  Name: AWSManagedRulesATPRuleSet
  ManagedRuleGroupConfigs:
    - LoginPath: /api/accounts/login
    - PayloadType: JSON
    - PasswordField:
        Identifier: /form/password
    - UsernameField:
        Identifier: /form/username
```

#### JSON<a name="aws-properties-wafv2-webacl-managedrulegroupstatement--examples--Configure_the_managed_rule_group_statement_for_AWSManagedRulesATPRuleSet_--json"></a>

```
{
  "ManagedRuleGroupStatement": {
    "VendorName": "AWS",
    "Name": "AWSManagedRulesATPRuleSet",
    "ManagedRuleGroupConfigs": [
      {
        "LoginPath": "/api/accounts/login"
      },
      {
        "PayloadType": "JSON"
      },
      {
        "PasswordField": {
          "Identifier": "/form/password"
        }
      },
      {
        "UsernameField": {
          "Identifier": "/form/username"
        }
      }
    ]
  }
}
```

### Configure a standard managed rule group statement<a name="aws-properties-wafv2-webacl-managedrulegroupstatement--examples--Configure_a_standard_managed_rule_group_statement_"></a>

The following shows an example `ManagedRuleGroupStatement` for a managed rule group that doesn't require additional configuration\. 

#### YAML<a name="aws-properties-wafv2-webacl-managedrulegroupstatement--examples--Configure_a_standard_managed_rule_group_statement_--yaml"></a>

```
ManagedRuleGroupStatement:
  VendorName: AWS
  Name: AWSManagedRulesCommonRuleSet
```

#### JSON<a name="aws-properties-wafv2-webacl-managedrulegroupstatement--examples--Configure_a_standard_managed_rule_group_statement_--json"></a>

```
{
  "ManagedRuleGroupStatement": {
    "VendorName": "AWS",
    "Name": "AWSManagedRulesCommonRuleSet"
  }
}
```