# Enable trusted access with AWS Organizations<a name="stacksets-orgs-enable-trusted-access"></a>

To set up the required permissions to create a stack set with **self\-managed** permissions, see [Grant self\-managed permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs-self-managed.html)\.

Before you create a stack set with **service\-managed** permissions, you must first complete the following tasks:
+ [Enable all features](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_org_support-all-features.html) in AWS Organizations\. With only consolidated billing features enabled, you cannot create a stack set with service\-managed permissions\.
+ Enable trusted access with AWS Organizations\. After trusted access is enabled, StackSets creates the necessary IAM roles in the organization's management account and target accounts when you create stack sets with service\-managed permissions\.
**Note**  
The IAM service\-linked role created in the management account has the suffix `CloudFormationStackSetsOrgAdmin`\. You can modify or delete this role only if trusted access with AWS Organizations is disabled\. The IAM service\-linked role created in each target account has the suffix `CloudFormationStackSetsOrgMember`\. You can modify or delete this role only if trusted access with AWS Organizations is disabled, or if the account is removed from the target organization or organizational unit \(OU\)\.

This topic describes how to enable trusted access with AWS Organizations\.

Only an account administrator in the management account has permissions to enable trusted access\. An *administrator user* is an *IAM user* with full permissions to your AWS account\. For more information, see [IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users) and [Creating your first IAM admin user and group](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html) in the IAM User Guide\.

**To enable trusted access in the **Create StackSet** wizard:**

See [Create a stack set with service\-managed permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html#create-stack-set-service-managed-permissions)\.

**To enable trusted access in the StackSets page of the AWS CloudFormation console:**

1. Determine which AWS account is the stack set's *administrator account*\. For stack sets with service\-managed permissions, the administrator account is the organization's management account\.

   Stack sets are created in the management account\. A *target account* is the account to which stack instances are deployed\.

1. Sign in to AWS as an administrator of the management account and open the AWS CloudFormation console at [https://console.aws.amazon.com/](https://console.aws.amazon.com/)\.

1. From the navigation pane, choose **StackSets**\. If trusted access is disabled, a banner displays that prompts you to enable trusted access\.  
![\[Enable trusted access banner.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-enable-trusted-access-from-stacksets-list.png)

1. Choose **Enable trusted access**\.

   Trusted access is successfully enabled when the following banner displays\.  
![\[Trusted access is successfully enabled banner.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-trusted-access-enabled-banner.png)

**To enable trusted access in the **Trusted access for AWS services** page of the AWS Organizations console:**

See [AWS CloudFormation StackSets and AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/services-that-can-integrate-cloudformation.html) in the AWS Organizations User Guide\.

**To disable trusted access:**

See [AWS CloudFormation StackSets and AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/services-that-can-integrate-cloudformation.html) in the AWS Organizations User Guide\. 