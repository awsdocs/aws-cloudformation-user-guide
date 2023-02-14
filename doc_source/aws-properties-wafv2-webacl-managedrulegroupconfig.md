# AWS::WAFv2::WebACL ManagedRuleGroupConfig<a name="aws-properties-wafv2-webacl-managedrulegroupconfig"></a>

Additional information that's used by a managed rule group\. Most managed rule groups don't require this\.

Use this for the account takeover prevention managed rule group `AWSManagedRulesATPRuleSet`, to provide information about the sign\-in page of your application\. 

You can provide multiple individual `ManagedRuleGroupConfig` objects for any rule group configuration, for example `UsernameField` and `PasswordField`\. The configuration that you provide depends on the needs of the managed rule group\. For the ATP managed rule group, you provide the following individual configuration objects: `LoginPath`, `PasswordField`, `PayloadType` and `UsernameField`\.

## Syntax<a name="aws-properties-wafv2-webacl-managedrulegroupconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-managedrulegroupconfig-syntax.json"></a>

```
{
  "[LoginPath](#cfn-wafv2-webacl-managedrulegroupconfig-loginpath)" : String,
  "[PasswordField](#cfn-wafv2-webacl-managedrulegroupconfig-passwordfield)" : FieldIdentifier,
  "[PayloadType](#cfn-wafv2-webacl-managedrulegroupconfig-payloadtype)" : String,
  "[UsernameField](#cfn-wafv2-webacl-managedrulegroupconfig-usernamefield)" : FieldIdentifier
}
```

### YAML<a name="aws-properties-wafv2-webacl-managedrulegroupconfig-syntax.yaml"></a>

```
  [LoginPath](#cfn-wafv2-webacl-managedrulegroupconfig-loginpath): String
  [PasswordField](#cfn-wafv2-webacl-managedrulegroupconfig-passwordfield): 
    FieldIdentifier
  [PayloadType](#cfn-wafv2-webacl-managedrulegroupconfig-payloadtype): String
  [UsernameField](#cfn-wafv2-webacl-managedrulegroupconfig-usernamefield): 
    FieldIdentifier
```

## Properties<a name="aws-properties-wafv2-webacl-managedrulegroupconfig-properties"></a>

`LoginPath`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-loginpath"></a>
The path of the login endpoint for your application\. For example, for the URL `https://example.com/web/login`, you would provide the path `/web/login`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PasswordField`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-passwordfield"></a>
Details about your login page password field\.   
*Required*: No  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadType`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-payloadtype"></a>
The payload type for your login endpoint, either JSON or form encoded\.  
*Required*: No  
*Type*: String  
*Allowed values*: `FORM_ENCODED | JSON`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsernameField`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-usernamefield"></a>
Details about your login page username field\.   
*Required*: No  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)