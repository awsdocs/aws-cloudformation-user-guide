# AWS::Config::OrganizationConfigRule<a name="aws-resource-config-organizationconfigrule"></a>

An organization config rule that has information about config rules that AWS Config creates in member accounts\. Only a master account can create or update an organization config rule\. 

`OrganizationConfigRule` resource enables organization service access through `EnableAWSServiceAccess` action and creates a service linked role in the master account of your organization\. The service linked role is created only when the role does not exist in the master account\. AWS Config verifies the existence of role with `GetRole` action\. 

## Syntax<a name="aws-resource-config-organizationconfigrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-organizationconfigrule-syntax.json"></a>

```
{
  "Type" : "AWS::Config::OrganizationConfigRule",
  "Properties" : {
      "[ExcludedAccounts](#cfn-config-organizationconfigrule-excludedaccounts)" : [ String, ... ],
      "[OrganizationConfigRuleName](#cfn-config-organizationconfigrule-organizationconfigrulename)" : String,
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
  [OrganizationCustomRuleMetadata](#cfn-config-organizationconfigrule-organizationcustomrulemetadata): 
    OrganizationCustomRuleMetadata
  [OrganizationManagedRuleMetadata](#cfn-config-organizationconfigrule-organizationmanagedrulemetadata): 
    OrganizationManagedRuleMetadata
```

## Properties<a name="aws-resource-config-organizationconfigrule-properties"></a>

`ExcludedAccounts`  <a name="cfn-config-organizationconfigrule-excludedaccounts"></a>
A comma\-separated list of accounts excluded from organization config rule\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationConfigRuleName`  <a name="cfn-config-organizationconfigrule-organizationconfigrulename"></a>
The name that you assign to organization config rule\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

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