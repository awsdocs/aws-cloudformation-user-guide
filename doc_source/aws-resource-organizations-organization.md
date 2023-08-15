# AWS::Organizations::Organization<a name="aws-resource-organizations-organization"></a>

Creates an AWS organization\. The account whose user is calling the [https://docs.aws.amazon.com/organizations/latest/APIReference/API_CreateOrganization.html](https://docs.aws.amazon.com/organizations/latest/APIReference/API_CreateOrganization.html) operation automatically becomes the [management account](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_getting-started_concepts.html#account) of the new organization\.

This operation must be called using credentials from the account that is to become the new organization's management account\. The principal must also have the [relevant IAM permissions](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_org_create.html)\.

**Important**  
If you delete an organization, you can't recover it\. If you created any policies inside of the organization, they're also deleted and you can't recover them\.
You can delete an organization only after you remove all member accounts from the organization\. If you created some of your member accounts using AWS Organizations, you might be blocked from removing those accounts\. You can remove a member account only if it has all the information that's required to operate as a standalone AWS account\. For more information about how to provide that information and then remove the account, see [Leave an organization from your member account](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_leave-as-member.html) in the * AWS Organizations User Guide*\.
If you closed a member account before you remove it from the organization, it enters a 'suspended' state for a period of time and you can't remove the account from the organization until it is finally closed\. This can take up to 90 days and can prevent you from deleting the organization until all member accounts are completely closed\.
For more information, see [Deleting an organization](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_org_delete.html) in the * AWS Organizations User Guide*\.

## Syntax<a name="aws-resource-organizations-organization-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-organizations-organization-syntax.json"></a>

```
{
  "Type" : "AWS::Organizations::Organization",
  "Properties" : {
      "[FeatureSet](#cfn-organizations-organization-featureset)" : String
    }
}
```

### YAML<a name="aws-resource-organizations-organization-syntax.yaml"></a>

```
Type: AWS::Organizations::Organization
Properties: 
  [FeatureSet](#cfn-organizations-organization-featureset): String
```

## Properties<a name="aws-resource-organizations-organization-properties"></a>

`FeatureSet`  <a name="cfn-organizations-organization-featureset"></a>
Specifies the feature set supported by the new organization\. Each feature set supports different levels of functionality\.  
+  `ALL` – In addition to all the features supported by the consolidated billing feature set, the management account gains access to advanced features that give you more control over accounts in your organization\. By default or if you set the `FeatureSet` property to `ALL`, the new organization is created with all features enabled and service control policies automatically enabled in the [root](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_getting-started_concepts.html#root)\. For more information, see [All features](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_getting-started_concepts.html#feature-set-all) in the * AWS Organizations User Guide*\.
+  `CONSOLIDATED_BILLING` – All member accounts have their bills consolidated to and paid by the management account\. For more information, see [Consolidated billing](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_getting-started_concepts.html#feature-set-cb-only) in the * AWS Organizations User Guide*\. 

   The consolidated billing feature subset isn't available for organizations in the AWS GovCloud \(US\) Region\.
Feature set `ALL` provides the following advanced features:  
+ Apply any [policy type](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies.html#orgs-policy-types) to any member account in the organization\. 
+ Apply [service control policies \(SCPs\)](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html) to member accounts that restrict the services and actions that users \(including the root user\) and roles in an account can access\. Using SCPs you can prevent member accounts from leaving the organization\.
+ Enable [integration with supported AWS services](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_integrate_services_list.html) to let those services provide functionality across all of the accounts in your organization\. 
If you don't specify this property, the default value is `ALL`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ALL | CONSOLIDATED_BILLING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-organizations-organization-return-values"></a>

### Ref<a name="aws-resource-organizations-organization-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the `AccountId`\. For example: `123456789012`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-organizations-organization-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-organizations-organization-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of an organization\.  


`Id`  <a name="Id-fn::getatt"></a>
The unique identifier \(ID\) of an organization\.  


`ManagementAccountArn`  <a name="ManagementAccountArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the account that is designated as the management account for the organization\.  


`ManagementAccountEmail`  <a name="ManagementAccountEmail-fn::getatt"></a>
The email address that is associated with the AWS account that is designated as the management account for the organization\.

`ManagementAccountId`  <a name="ManagementAccountId-fn::getatt"></a>
The unique identifier \(ID\) of the management account of an organization\.  


`RootId`  <a name="RootId-fn::getatt"></a>
The unique identifier \(ID\) for the root\.  


## Examples<a name="aws-resource-organizations-organization--examples"></a>



### Organization FeatureSet specified as ALL<a name="aws-resource-organizations-organization--examples--Organization_FeatureSet_specified_as_ALL"></a>

This example illustrates how to specify the organization feature set as `ALL` in `AWS::Organizations::Organization`\.

#### JSON<a name="aws-resource-organizations-organization--examples--Organization_FeatureSet_specified_as_ALL--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "AWS CloudFormation Organizations Template Example",
  "Resources": {
    "OrganizationTemplateExample": {
      "DeletionPolicy": "Retain",
      "Type": "AWS::Organizations::Organization",
      "Properties": {
        "FeatureSet": "ALL"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-organizations-organization--examples--Organization_FeatureSet_specified_as_ALL--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS CloudFormation Organizations Template Example
Resources:
  OrganizationTemplateExample:
    DeletionPolicy: Retain
    Type: 'AWS::Organizations::Organization'
    Properties:
      FeatureSet: ALL
```

### Organization FeatureSet specified as CONSOLIDATED\_BILLING<a name="aws-resource-organizations-organization--examples--Organization_FeatureSet_specified_as_CONSOLIDATED_BILLING"></a>

This example illustrates how to specify the organization feature set as `CONSOLIDATED_BILLING` in `AWS::Organizations::Organization`\.

#### JSON<a name="aws-resource-organizations-organization--examples--Organization_FeatureSet_specified_as_CONSOLIDATED_BILLING--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "AWS CloudFormation Organizations Template Example",
  "Resources": {
    "OrganizationTemplateExample": {
      "DeletionPolicy": "Retain",
      "Type": "AWS::Organizations::Organization",
      "Properties": {
        "FeatureSet": "CONSOLIDATED_BILLING"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-organizations-organization--examples--Organization_FeatureSet_specified_as_CONSOLIDATED_BILLING--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: AWS CloudFormation Organizations Template Example
Resources:
  OrganizationTemplateExample:
    DeletionPolicy: Retain
    Type: 'AWS::Organizations::Organization'
    Properties:
      FeatureSet: CONSOLIDATED_BILLING
```

## See also<a name="aws-resource-organizations-organization--seealso"></a>
+ [Creating an organization](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_org_create.html) in the *AWS Organizations User Guide*\.
+ [CreateOrganization](https://docs.aws.amazon.com/organizations/latest/APIReference/API_CreateOrganization.html) in the *AWS Organizations API Reference Guide*\.

