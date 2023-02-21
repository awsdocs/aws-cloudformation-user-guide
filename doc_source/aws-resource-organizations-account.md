# AWS::Organizations::Account<a name="aws-resource-organizations-account"></a>

Creates an AWS account that is automatically a member of the organization whose credentials made the request\.

 AWS CloudFormation uses the [https://docs.aws.amazon.com/organizations/latest/APIReference/API_CreateAccount.html](https://docs.aws.amazon.com/organizations/latest/APIReference/API_CreateAccount.html) operation to create accounts\. This is an asynchronous request that AWS performs in the background\. Because `CreateAccount` operates asynchronously, it can return a successful completion message even though account initialization might still be in progress\. You might need to wait a few minutes before you can successfully access the account\. To check the status of the request, do one of the following:
+ Use the `Id` value of the `CreateAccountStatus` response element from the `CreateAccount` operation to provide as a parameter to the [https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribeCreateAccountStatus.html](https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribeCreateAccountStatus.html) operation\.
+ Check the CloudTrail log for the `CreateAccountResult` event\. For information on using CloudTrail with AWS Organizations, see [Logging and monitoring in AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_security_incident-response.html#orgs_cloudtrail-integration) in the * AWS Organizations User Guide\.* 

The user who calls the API to create an account must have the `organizations:CreateAccount` permission\. If you enabled all features in the organization, AWS Organizations creates the required service\-linked role named `AWSServiceRoleForOrganizations`\. For more information, see [AWS Organizations and Service\-Linked Roles](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_integrate_services.html#orgs_integrate_services-using_slrs) in the * AWS Organizations User Guide*\.

If the request includes tags, then the requester must have the `organizations:TagResource` permission\.

 AWS Organizations preconfigures the new member account with a role \(named `OrganizationAccountAccessRole` by default\) that grants users in the management account administrator permissions in the new member account\. Principals in the management account can assume the role\. AWS Organizations clones the company name and address information for the new account from the organization's management account\.

For more information about creating accounts, see [Creating an AWS account in Your Organization](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_create.html) in the * AWS Organizations User Guide\.* 

This operation can be called only from the organization's management account\.

**Deleting Account resources**

The default `DeletionPolicy` for resource `AWS::Organizations::Account` is `Retain`\. For more information about how AWS CloudFormation deletes resources, see [ DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

**Important**  
If you include multiple accounts in a single template, you must use the `DependsOn` attribute on each account resource type so that the accounts are created sequentially\. If you create multiple accounts at the same time, Organizations returns an error and the stack operation fails\.
You can't modify the following list of `Account` resource parameters using AWS CloudFormation updates\.  
AccountName
Email
RoleName
If you attempt to update the listed parameters, CloudFormation will attempt the update, but you will receive an error message as those updates are not supported from an Organizations management account or a [registered delegated administrator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-delegated-admin.html) account\. Both the update and the update roll\-back will fail, so you must skip the account resource update\. To update parameters `AccountName` and `Email`, you must sign in to the AWS Management Console as the AWS account root user\. For more information, see [Modifying the account name, email address, or password for the AWS account root user](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-root-user.html) in the *AWS Account Management Reference Guide*\.
When you create an account in an organization using the AWS Organizations console, API, or AWS CLI commands, we don't automatically collect the information required for the account to operate as a standalone account\. That includes collecting the payment method and signing the end user license agreement \(EULA\)\. If you must remove an account from your organization later, you can do so only after you provide the missing information\. Follow the steps at [ To leave an organization as a member account](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_remove.html#leave-without-all-info) in the * AWS Organizations User Guide*\.
When you create an account in an organization using AWS CloudFormation, you can't specify a value for the `CreateAccount` operation parameter `IamUserAccessToBilling`\. The default value for parameter `IamUserAccessToBilling` is `ALLOW`, and IAM users and roles with the required permissions can access billing information for the new account\.
If you get an exception that indicates `DescribeCreateAccountStatus returns IN_PROGRESS state before time out`\. You must check the account creation status using the [https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribeCreateAccountStatus.html](https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribeCreateAccountStatus.html) operation\. If the account state returns as `SUCCEEDED`, you can import the account into AWS CloudFormation management using [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import.html)\.
If you get an exception that indicates you have exceeded your account quota for the organization, you can request an increase by using the [Service Quotas console](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_reference_limits.html)\.
If you get an exception that indicates the operation failed because your organization is still initializing, wait one hour and then try again\. If the error persists, contact [AWS Support](https://console.aws.amazon.com/support/home#/)\.
We don't recommend that you use the `CreateAccount` operation to create multiple temporary accounts\. You can close accounts using the [https://docs.aws.amazon.com/organizations/latest/APIReference/API_CloseAccount.html](https://docs.aws.amazon.com/organizations/latest/APIReference/API_CloseAccount.html) operation or from the AWS Organizations console in the organization's management account\. For information on the requirements and process for closing an account, see [Closing an AWS account](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_close.html) in the * AWS Organizations User Guide*\.

## Syntax<a name="aws-resource-organizations-account-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-organizations-account-syntax.json"></a>

```
{
  "Type" : "AWS::Organizations::Account",
  "Properties" : {
      "[AccountName](#cfn-organizations-account-accountname)" : String,
      "[Email](#cfn-organizations-account-email)" : String,
      "[ParentIds](#cfn-organizations-account-parentids)" : [ String, ... ],
      "[RoleName](#cfn-organizations-account-rolename)" : String,
      "[Tags](#cfn-organizations-account-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-organizations-account-syntax.yaml"></a>

```
Type: AWS::Organizations::Account
Properties: 
  [AccountName](#cfn-organizations-account-accountname): String
  [Email](#cfn-organizations-account-email): String
  [ParentIds](#cfn-organizations-account-parentids): 
    - String
  [RoleName](#cfn-organizations-account-rolename): String
  [Tags](#cfn-organizations-account-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-organizations-account-properties"></a>

`AccountName`  <a name="cfn-organizations-account-accountname"></a>
The account name given to the account when it was created\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Pattern*: `[\u0020-\u007E]+`  
*Update requires*: Updates are not supported\.

`Email`  <a name="cfn-organizations-account-email"></a>
The email address associated with the AWS account\.  
The [regex pattern](http://wikipedia.org/wiki/regex) for this parameter is a string of characters that represents a standard internet email address\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `64`  
*Pattern*: `[^\s@]+@[^\s@]+\.[^\s@]+`  
*Update requires*: Updates are not supported\.

`ParentIds`  <a name="cfn-organizations-account-parentids"></a>
The unique identifier \(ID\) of the root or organizational unit \(OU\) that you want to create the new account in\. If you don't specify this parameter, the `ParentId` defaults to the root ID\.  
This parameter only accepts a string array with one string value\.  
The [regex pattern](http://wikipedia.org/wiki/regex) for a parent ID string requires one of the following:  
+  **Root** \- A string that begins with "r\-" followed by from 4 to 32 lowercase letters or digits\.
+  **Organizational unit \(OU\)** \- A string that begins with "ou\-" followed by from 4 to 32 lowercase letters or digits \(the ID of the root that the OU is in\)\. This string is followed by a second "\-" dash and from 8 to 32 additional lowercase letters or digits\.
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Pattern*: `^(r-[0-9a-z]{4,32})|(ou-[0-9a-z]{4,32}-[a-z0-9]{8,32})$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleName`  <a name="cfn-organizations-account-rolename"></a>
The name of an IAM role that AWS Organizations automatically preconfigures in the new member account\. This role trusts the management account, allowing users in the management account to assume the role, as permitted by the management account administrator\. The role has administrator permissions in the new member account\.  
If you don't specify this parameter, the role name defaults to `OrganizationAccountAccessRole`\.  
For more information about how to use this role to access the member account, see the following links:  
+  [Accessing and Administering the Member Accounts in Your Organization](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_access.html#orgs_manage_accounts_create-cross-account-role) in the * AWS Organizations User Guide* 
+ Steps 2 and 3 in [Tutorial: Delegate Access Across AWS accounts Using IAM Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/tutorial_cross-account-with-roles.html) in the *IAM User Guide* 
The [regex pattern](http://wikipedia.org/wiki/regex) that is used to validate this parameter\. The pattern can include uppercase letters, lowercase letters, digits with no spaces, and any of the following characters: =,\.@\-  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Pattern*: `[\w+=,.@-]{1,64}`  
*Update requires*: Updates are not supported\.

`Tags`  <a name="cfn-organizations-account-tags"></a>
A list of tags that you want to attach to the newly created account\. For each tag in the list, you must specify both a tag key and a value\. You can set the value to an empty string, but you can't set it to `null`\. For more information about tagging, see [Tagging AWS Organizations resources](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_tagging.html) in the AWS Organizations User Guide\.  
If any one of the tags is not valid or if you exceed the maximum allowed number of tags for an account, then the entire request fails and the account is not created\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-organizations-account-return-values"></a>

### Ref<a name="aws-resource-organizations-account-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `AccountId`\. For example: `123456789012`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-organizations-account-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-organizations-account-return-values-fn--getatt-fn--getatt"></a>

`AccountId`  <a name="AccountId-fn::getatt"></a>
Returns the unique identifier \(ID\) of the account\. For example: `123456789012`\.

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the account\. For example: `arn:aws:organizations::111111111111:account/o-exampleorgid/555555555555`\.

`JoinedMethod`  <a name="JoinedMethod-fn::getatt"></a>
Returns the method by which the account joined the organization\. For example: `INVITED | CREATED`\.

`JoinedTimestamp`  <a name="JoinedTimestamp-fn::getatt"></a>
Returns the date the account became a part of the organization\. For example: `2016-11-24T11:11:48-08:00`\.

`Status`  <a name="Status-fn::getatt"></a>
Returns the status of the account in the organization\. For example: `ACTIVE | SUSPENDED | PENDING_CLOSURE`\.