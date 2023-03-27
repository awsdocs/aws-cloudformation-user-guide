# AWS::WAFv2::WebACL ManagedRuleGroupConfig<a name="aws-properties-wafv2-webacl-managedrulegroupconfig"></a>

Additional information that's used by a managed rule group\. Many managed rule groups don't require this\.

Use the `AWSManagedRulesBotControlRuleSet` configuration object to configure the protection level that you want the Bot Control rule group to use\. 

## Syntax<a name="aws-properties-wafv2-webacl-managedrulegroupconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-managedrulegroupconfig-syntax.json"></a>

```
{
  "[AWSManagedRulesATPRuleSet](#cfn-wafv2-webacl-managedrulegroupconfig-awsmanagedrulesatpruleset)" : AWSManagedRulesATPRuleSet,
  "[AWSManagedRulesBotControlRuleSet](#cfn-wafv2-webacl-managedrulegroupconfig-awsmanagedrulesbotcontrolruleset)" : AWSManagedRulesBotControlRuleSet,
  "[LoginPath](#cfn-wafv2-webacl-managedrulegroupconfig-loginpath)" : String,
  "[PasswordField](#cfn-wafv2-webacl-managedrulegroupconfig-passwordfield)" : FieldIdentifier,
  "[PayloadType](#cfn-wafv2-webacl-managedrulegroupconfig-payloadtype)" : String,
  "[UsernameField](#cfn-wafv2-webacl-managedrulegroupconfig-usernamefield)" : FieldIdentifier
}
```

### YAML<a name="aws-properties-wafv2-webacl-managedrulegroupconfig-syntax.yaml"></a>

```
  [AWSManagedRulesATPRuleSet](#cfn-wafv2-webacl-managedrulegroupconfig-awsmanagedrulesatpruleset): 
    AWSManagedRulesATPRuleSet
  [AWSManagedRulesBotControlRuleSet](#cfn-wafv2-webacl-managedrulegroupconfig-awsmanagedrulesbotcontrolruleset): 
    AWSManagedRulesBotControlRuleSet
  [LoginPath](#cfn-wafv2-webacl-managedrulegroupconfig-loginpath): String
  [PasswordField](#cfn-wafv2-webacl-managedrulegroupconfig-passwordfield): 
    FieldIdentifier
  [PayloadType](#cfn-wafv2-webacl-managedrulegroupconfig-payloadtype): String
  [UsernameField](#cfn-wafv2-webacl-managedrulegroupconfig-usernamefield): 
    FieldIdentifier
```

## Properties<a name="aws-properties-wafv2-webacl-managedrulegroupconfig-properties"></a>

`AWSManagedRulesATPRuleSet`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-awsmanagedrulesatpruleset"></a>
Additional configuration for using the account takeover prevention \(ATP\) managed rule group, `AWSManagedRulesATPRuleSet`\. Use this to provide login request information to the rule group\. For web ACLs that protect CloudFront distributions, use this to also provide the information about how your distribution responds to login requests\.   
This configuration replaces the individual configuration fields in `ManagedRuleGroupConfig` and provides additional feature configuration\.   
For information about using the ATP managed rule group, see [AWS WAF Fraud Control account takeover prevention \(ATP\) rule group](https://docs.aws.amazon.com/waf/latest/developerguide/aws-managed-rule-groups-atp.html) and [AWS WAF Fraud Control account takeover prevention \(ATP\)](https://docs.aws.amazon.com/waf/latest/developerguide/waf-atp.html) in the * AWS WAF Developer Guide*\.  
*Required*: No  
*Type*: [AWSManagedRulesATPRuleSet](aws-properties-wafv2-webacl-awsmanagedrulesatpruleset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AWSManagedRulesBotControlRuleSet`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-awsmanagedrulesbotcontrolruleset"></a>
Additional configuration for using the Bot Control managed rule group\. Use this to specify the inspection level that you want to use\. For information about using the Bot Control managed rule group, see [AWS WAF Bot Control rule group](https://docs.aws.amazon.com/waf/latest/developerguide/aws-managed-rule-groups-bot.html) and [AWS WAF Bot Control](https://docs.aws.amazon.com/waf/latest/developerguide/waf-bot-control.html) in the * AWS WAF Developer Guide*\.  
*Required*: No  
*Type*: [AWSManagedRulesBotControlRuleSet](aws-properties-wafv2-webacl-awsmanagedrulesbotcontrolruleset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoginPath`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-loginpath"></a>
Instead of this setting, provide your configuration under `AWSManagedRulesATPRuleSet`\. 
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PasswordField`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-passwordfield"></a>
Instead of this setting, provide your configuration under `AWSManagedRulesATPRuleSet` `RequestInspection`\. 
*Required*: No  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadType`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-payloadtype"></a>
Instead of this setting, provide your configuration under `AWSManagedRulesATPRuleSet` `RequestInspection`\. 
*Required*: No  
*Type*: String  
*Allowed values*: `FORM_ENCODED | JSON`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsernameField`  <a name="cfn-wafv2-webacl-managedrulegroupconfig-usernamefield"></a>
Instead of this setting, provide your configuration under `AWSManagedRulesATPRuleSet` `RequestInspection`\. 
*Required*: No  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)