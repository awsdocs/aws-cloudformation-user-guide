# Activate trusted access with AWS Organizations<a name="stacksets-orgs-activate-trusted-access"></a>

To set up the required permissions to create a stack set with **self\-managed** permissions, see [Grant self\-managed permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs-self-managed.html)\.

Before you create a stack set with **service\-managed** permissions, you must first complete the following tasks:
+ [Enable all features](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_org_support-all-features.html) in AWS Organizations\. With only consolidated billing features enabled, you cannot create a stack set with service\-managed permissions\.
+ Activate trusted access with AWS Organizations\. After trusted access is activated, StackSets creates the necessary IAM roles in the organization's management account and target \(member\) accounts when you create stack sets with service\-managed permissions\.
**Note**  
The IAM service\-linked role created in the management account has the suffix `CloudFormationStackSetsOrgAdmin`\. You can modify or delete this role only if trusted access with AWS Organizations is deactivated\. The IAM service\-linked role created in each target account has the suffix `CloudFormationStackSetsOrgMember`\. You can modify or delete this role only if trusted access with AWS Organizations is deactivated, or if the account is removed from the target organization or organizational unit \(OU\)\.

For more information for managing trusted access with APIs, see:
+ [ActivateOrganizationsAccess](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ActivateOrganizationsAccess.html)
+ [DeactivateOrganizationsAccess](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeactivateOrganizationsAccess.html)
+ [DescribeOrganizationsAccess](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeOrganizationsAccess.html)

Only an account administrator in the management account has permissions to activate trusted access\. An *administrator user* is an *IAM user* with full permissions to your AWS account\. For more information, see [IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users) and [Creating your first IAM admin user and group](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html) in the *IAM User Guide*\.

With trusted access activated, the management account and delegated administrator accounts can create and manage service\-managed stack sets for their organization\.

**To activate trusted access in the **Create StackSet** wizard**

See [Create a stack set with service\-managed permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html#create-stack-set-service-managed-permissions)\.

**To activate trusted access using the AWS CloudFormation console**

1. Sign in to AWS as an administrator of the management account and open the AWS CloudFormation console at [https://console.aws.amazon.com/](https://console.aws.amazon.com/)\.

1. From the navigation pane, choose **StackSets**\. If trusted access is deactivated, a banner displays that prompts you to activate trusted access\.  
![\[Activate trusted access banner.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-enable-trusted-access-from-stacksets-list-new.png)

1. Choose **Activate trusted access**\.

   Trusted access is successfully activated when the following banner displays\.  
![\[Trusted access is successfully activated banner.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-trusted-access-enabled-banner-new.png)
**Note**  
Activate Organizations Access is the same as Enable Organizations Access, and Deactivate Organizations Access is the same as Disable Organizations Access\. These terms have been updated based on marketing guidelines\. 

**To activate trusted access in the **Trusted access for AWS services** page of the AWS Organizations console**

See [AWS CloudFormation StackSets and AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/services-that-can-integrate-cloudformation.html) in the *AWS Organizations User Guide*\.

**To deactivate trusted access**

See [AWS CloudFormation StackSets and AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/services-that-can-integrate-cloudformation.html) in the *AWS Organizations User Guide*\.

Before you can deactivate trusted access with AWS Organizations, you must deregister all delegated administrators\. For more information, see [Register a delegated administrator](stacksets-orgs-delegated-admin.md)\.