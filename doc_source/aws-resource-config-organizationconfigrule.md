# AWS::Config::OrganizationConfigRule<a name="aws-resource-config-organizationconfigrule"></a>

Adds or updates an AWS Config rule for your entire organization to evaluate if your AWS resources comply with your desired configurations\. For information on how many organization AWS Config rules you can have per account, see [https://docs.aws.amazon.com/config/latest/developerguide/configlimits.html](https://docs.aws.amazon.com/config/latest/developerguide/configlimits.html) in the *AWS Config Developer Guide*\.

 Only a management account and a delegated administrator can create or update an organization AWS Config rule\. When calling the `OrganizationConfigRule` resource with a delegated administrator, you must ensure AWS Organizations `ListDelegatedAdministrator` permissions are added\. An organization can have up to 3 delegated administrators\.

The `OrganizationConfigRule` resource enables organization service access through the `EnableAWSServiceAccess` action and creates a service\-linked role `AWSServiceRoleForConfigMultiAccountSetup` in the management or delegated administrator account of your organization\. The service\-linked role is created only when the role does not exist in the caller account\. AWS Config verifies the existence of role with `GetRole` action\.

To use the `OrganizationConfigRule` resource with delegated administrator, register a delegated administrator by calling AWS Organization `register-delegated-administrator` for `config-multiaccountsetup.amazonaws.com`\. 

There are two types of rules: *AWS Config Managed Rules* and *AWS Config Custom Rules*\. You can use `PutOrganizationConfigRule` to create both AWS Config Managed Rules and AWS Config Custom Rules\.

AWS Config Managed Rules are predefined, customizable rules created by AWS Config\. For a list of managed rules, see [List of AWS Config Managed Rules](https://docs.aws.amazon.com/config/latest/developerguide/managed-rules-by-aws-config.html)\. If you are adding an AWS Config managed rule, you must specify the rule's identifier for the `RuleIdentifier` key\.

AWS Config Custom Rules are rules that you create from scratch\. There are two ways to create AWS Config custom rules: with Lambda functions \([AWS Lambda Developer Guide](https://docs.aws.amazon.com/config/latest/developerguide/gettingstarted-concepts.html#gettingstarted-concepts-function)\) and with Guard \([Guard GitHub Repository](https://github.com/aws-cloudformation/cloudformation-guard)\), a policy\-as\-code language\. AWS Config custom rules created with AWS Lambda are called *AWS Config Custom Lambda Rules* and AWS Config custom rules created with Guard are called *AWS Config Custom Policy Rules*\.

If you are adding a new AWS Config Custom Lambda rule, you first need to create an AWS Lambda function in the management account or a delegated administrator that the rule invokes to evaluate your resources\. You also need to create an IAM role in the managed account that can be assumed by the Lambda function\. When you use `PutOrganizationConfigRule` to add a Custom Lambda rule to AWS Config, you must specify the Amazon Resource Name \(ARN\) that AWS Lambda assigns to the function\.

## Syntax<a name="aws-resource-config-organizationconfigrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-organizationconfigrule-syntax.json"></a>

```
{
  "Type" : "AWS::Config::OrganizationConfigRule",
  "Properties" : {
      "[ExcludedAccounts](#cfn-config-organizationconfigrule-excludedaccounts)" : [ String, ... ],
      "[OrganizationConfigRuleName](#cfn-config-organizationconfigrule-organizationconfigrulename)" : String,
      "[OrganizationCustomPolicyRuleMetadata](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata)" : OrganizationCustomPolicyRuleMetadata,
      "[OrganizationCustomRuleMetadata](#cfn-config-organizationconfigrule-organizationcustomrulemetadata)" : OrganizationCustomRuleMetadata,
      "[OrganizationManagedRuleMetadata](#cfn-config-organizationconfigrule-organizationmanagedrulemetadata)" : OrganizationManagedRuleMetadata
    }
}
```

### YAML<a name="aws-resource-config-organizationconfigrule-syntax.yaml"></a>

```
Type: AWS::Config::OrganizationConfigRule
Properties: 
  [ExcludedAccounts](#cfn-config-organizationconfigrule-excludedaccounts): 
    - String
  [OrganizationConfigRuleName](#cfn-config-organizationconfigrule-organizationconfigrulename): String
  [OrganizationCustomPolicyRuleMetadata](#cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata): 
    OrganizationCustomPolicyRuleMetadata
  [OrganizationCustomRuleMetadata](#cfn-config-organizationconfigrule-organizationcustomrulemetadata): 
    OrganizationCustomRuleMetadata
  [OrganizationManagedRuleMetadata](#cfn-config-organizationconfigrule-organizationmanagedrulemetadata): 
    OrganizationManagedRuleMetadata
```

## Properties<a name="aws-resource-config-organizationconfigrule-properties"></a>

`ExcludedAccounts`  <a name="cfn-config-organizationconfigrule-excludedaccounts"></a>
A comma\-separated list of accounts excluded from organization AWS Config rule\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationConfigRuleName`  <a name="cfn-config-organizationconfigrule-organizationconfigrulename"></a>
The name that you assign to organization AWS Config rule\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OrganizationCustomPolicyRuleMetadata`  <a name="cfn-config-organizationconfigrule-organizationcustompolicyrulemetadata"></a>
An object that specifies metadata for your organization's AWS Config Custom Policy rule\. The metadata includes the runtime system in use, which accounts have debug logging enabled, and other custom rule metadata, such as resource type, resource ID of AWS resource, and organization trigger types that initiate AWS Config to evaluate AWS resources against a rule\.  
*Required*: No  
*Type*: [OrganizationCustomPolicyRuleMetadata](aws-properties-config-organizationconfigrule-organizationcustompolicyrulemetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationCustomRuleMetadata`  <a name="cfn-config-organizationconfigrule-organizationcustomrulemetadata"></a>
An `OrganizationCustomRuleMetadata` object\.  
*Required*: No  
*Type*: [OrganizationCustomRuleMetadata](aws-properties-config-organizationconfigrule-organizationcustomrulemetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationManagedRuleMetadata`  <a name="cfn-config-organizationconfigrule-organizationmanagedrulemetadata"></a>
An `OrganizationManagedRuleMetadata` object\.  
*Required*: No  
*Type*: [OrganizationManagedRuleMetadata](aws-properties-config-organizationconfigrule-organizationmanagedrulemetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-config-organizationconfigrule-return-values"></a>

### Ref<a name="aws-resource-config-organizationconfigrule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the OrganizationConfigRuleName\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-config-organizationconfigrule--examples"></a>



### Managed Rule<a name="aws-resource-config-organizationconfigrule--examples--Managed_Rule"></a>

The following example creates a managed organization config rule\.

#### JSON<a name="aws-resource-config-organizationconfigrule--examples--Managed_Rule--json"></a>

```
{
    "BasicOrganizationConfigRule": {
        "Type": "AWS::Config::OrganizationConfigRule",
        "Properties": {
            "OrganizationConfigRuleName": "OrganizationConfigRuleName",
            "OrganizationManagedRuleMetadata": {
                "RuleIdentifier": "CLOUD_TRAIL_ENABLED",
                "Description": "Cloudtrail enabled rule"
            },
            "ExcludedAccounts": [
                "accountId"
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-config-organizationconfigrule--examples--Managed_Rule--yaml"></a>

```
BasicOrganizationConfigRule:
    Type: "AWS::Config::OrganizationConfigRule"
    Properties:
        OrganizationConfigRuleName: "OrganizationConfigRuleName"
        OrganizationManagedRuleMetadata:
            RuleIdentifier: "CLOUD_TRAIL_ENABLED"
            Description: "Cloudtrail enabled rule"
        ExcludedAccounts:
        - "accountId"
```

### Custom Rule<a name="aws-resource-config-organizationconfigrule--examples--Custom_Rule"></a>

The following example creates a custom organization config rule\.

#### JSON<a name="aws-resource-config-organizationconfigrule--examples--Custom_Rule--json"></a>

```
{
    "BasicOrganizationConfigRule": {
        "Type": "AWS::Config::OrganizationConfigRule",
        "Properties": {
            "OrganizationConfigRuleName": "OrganizationConfigRuleName",
            "OrganizationCustomRuleMetadata": {
                "LambdaFunctionArn": "CustomRuleLambdaArn",
                "OrganizationConfigRuleTriggerTypes": [
                    "ScheduledNotification"
                ]
            },
            "ExcludedAccounts": [
                "accountId"
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-config-organizationconfigrule--examples--Custom_Rule--yaml"></a>

```
BasicOrganizationConfigRule:
    Type: "AWS::Config::OrganizationConfigRule"
    Properties:
        OrganizationConfigRuleName: "OrganizationConfigRuleName"
        OrganizationCustomRuleMetadata:
            LambdaFunctionArn: "CustomRuleLambdaArn"
            OrganizationConfigRuleTriggerTypes:
                - "ScheduledNotification"
            ExcludedAccounts:
            - "accountId"
```