# AWS::Config::OrganizationConfigRule OrganizationCustomPolicyRuleMetadata<a name="aws-properties-config-organizationconfigrule-organizationcustompolicyrulemetadata"></a>

An object that specifies metadata for your organization's AWS Config Custom Policy rule\. The metadata includes the runtime system in use, which accounts have debug logging enabled, and other custom rule metadata, such as resource type, resource ID of AWS resource, and organization trigger types that initiate AWS Config to evaluate AWS resources against a rule\.

## Syntax<a name="aws-properties-config-organizationconfigrule-organizationcustompolicyrulemetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-organizationconfigrule-organizationcustompolicyrulemetadata-syntax.json"></a>

```
{
  "[DebugLogDeliveryAccounts](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-debuglogdeliveryaccounts)" : [ String, ... ],
  "[Description](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-description)" : String,
  "[InputParameters](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-inputparameters)" : String,
  "[MaximumExecutionFrequency](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-maximumexecutionfrequency)" : String,
  "[OrganizationConfigRuleTriggerTypes](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-organizationconfigruletriggertypes)" : [ String, ... ],
  "[PolicyText](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-policytext)" : String,
  "[ResourceIdScope](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-resourceidscope)" : String,
  "[ResourceTypesScope](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-resourcetypesscope)" : [ String, ... ],
  "[Runtime](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-runtime)" : String,
  "[TagKeyScope](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-tagkeyscope)" : String,
  "[TagValueScope](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-tagvaluescope)" : String
}
```

### YAML<a name="aws-properties-config-organizationconfigrule-organizationcustompolicyrulemetadata-syntax.yaml"></a>

```
  [DebugLogDeliveryAccounts](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-debuglogdeliveryaccounts): 
    - String
  [Description](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-description): String
  [InputParameters](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-inputparameters): String
  [MaximumExecutionFrequency](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-maximumexecutionfrequency): String
  [OrganizationConfigRuleTriggerTypes](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-organizationconfigruletriggertypes): 
    - String
  [PolicyText](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-policytext): String
  [ResourceIdScope](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-resourceidscope): String
  [ResourceTypesScope](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-resourcetypesscope): 
    - String
  [Runtime](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-runtime): String
  [TagKeyScope](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-tagkeyscope): String
  [TagValueScope](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-tagvaluescope): String
```

## Properties<a name="aws-properties-config-organizationconfigrule-organizationcustompolicyrulemetadata-properties"></a>

`DebugLogDeliveryAccounts`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-debuglogdeliveryaccounts"></a>
A list of accounts that you can enable debug logging for your organization AWS Config Custom Policy rule\. List is null when debug logging is enabled for all accounts\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-description"></a>
The description that you provide for your organization AWS Config Custom Policy rule\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputParameters`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-inputparameters"></a>
A string, in JSON format, that is passed to your organization AWS Config Custom Policy rule\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumExecutionFrequency`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-maximumexecutionfrequency"></a>
The maximum frequency with which AWS Config runs evaluations for a rule\. Your AWS Config Custom Policy rule is triggered when AWS Config delivers the configuration snapshot\. For more information, see [ConfigSnapshotDeliveryProperties](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-deliverychannel.html#cfn-config-deliverychannel-configsnapshotdeliveryproperties)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `One_Hour | Six_Hours | Three_Hours | Twelve_Hours | TwentyFour_Hours`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationConfigRuleTriggerTypes`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-organizationconfigruletriggertypes"></a>
The type of notification that initiates AWS Config to run an evaluation for a rule\. For AWS Config Custom Policy rules, AWS Config supports change\-initiated notification types:  
+  `ConfigurationItemChangeNotification` \- Initiates an evaluation when AWS Config delivers a configuration item as a result of a resource change\.
+  `OversizedConfigurationItemChangeNotification` \- Initiates an evaluation when AWS Config delivers an oversized configuration item\. AWS Config may generate this notification type when a resource changes and the notification exceeds the maximum size allowed by Amazon SNS\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyText`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-policytext"></a>
The policy definition containing the logic for your organization AWS Config Custom Policy rule\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceIdScope`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-resourceidscope"></a>
The ID of the AWS resource that was evaluated\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `768`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTypesScope`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-resourcetypesscope"></a>
The type of the AWS resource that was evaluated\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Runtime`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-runtime"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagKeyScope`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-tagkeyscope"></a>
One part of a key\-value pair that make up a tag\. A key is a general label that acts like a category for more specific tag values\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagValueScope`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata-tagvaluescope"></a>
The optional part of a key\-value pair that make up a tag\. A value acts as a descriptor within a tag category \(key\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)