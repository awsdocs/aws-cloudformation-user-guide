# Register a delegated administrator<a name="stacksets-orgs-delegated-admin"></a>

In addition to your organization's management account, member accounts with delegated administrator permissions can create and manage stack sets with service\-managed permissions for the organization\. Stack sets with service\-managed permissions are created in the management account, including stack sets created by delegated administrators\. To be registered as a delegated administrator for your organization, your member account must be in the organization\. For more information about joining an organization, see [Inviting an AWS account to join your organization](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_invites.html)\.

Your organization can have up to five registered delegated administrators at one time\. Delegated administrators can choose to deploy to all accounts in your organization or specific OUs\. Trusted access with AWS Organizations must be enabled before delegated administrators can deploy to accounts managed by Organizations\. For more information, see [Enable trusted access with AWS Organizations](stacksets-orgs-enable-trusted-access.md)\.

**Important**  
Delegated administrators have full permissions to deploy to accounts in your organization\. The management account can't limit delegated administrator permissions to deploy to specific OUs or to perform specific stack set operations\.

You can register delegated administrators for your organization in the following Regions: US East \(Ohio\), US East \(N\. Virginia\), US West \(N\. California\), US West \(Oregon\), Asia Pacific \(Mumbai\), Asia Pacific \(Seoul\), Asia Pacific \(Singapore\), Asia Pacific \(Sydney\), Asia Pacific \(Tokyo\), Canada \(Central\), Europe \(Frankfurt\), Europe \(Ireland\), Europe \(London\), Europe \(Paris\), Europe \(Stockholm\), South America \(São Paulo\), AWS GovCloud \(US\-East\), and AWS GovCloud \(US\-West\)\.

You can register and deregister delegated administrators using the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation/), [AWS CLI](https://aws.amazon.com/cli/), or [AWS SDKs](https://aws.amazon.com/tools/)\.

**To register a delegated administrator \(console\)**

1. Sign in to AWS as an administrator of the management account and open the AWS CloudFormation console at [https://console.aws.amazon.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. Under **Delegated administrators**, choose **Register delegated administrator**\.

1. In the **Register delegated administrator** dialog box, choose **Register delegated administrator**\.

   The success message indicates that the member account has successfully been registered as a delegated administrator\.

**To deregister a delegated administrator \(console\)**

1. Sign in to AWS as an administrator of the management account and open the AWS CloudFormation console at [https://console.aws.amazon.com/](https://console.aws.amazon.com/)\.

1. From the navigation pane, choose **StackSets**\.

1. Under **Delegated administrators**, select the account that you want to deregister, and then choose **Deregister**\.

   The success message indicates that the member account has successfully been deregistered as a delegated administrator\.

   You can register this account again at any time\.

**To register a delegated administrator \(AWS CLI\)**

1. Open the AWS CLI\.

1. Run the `register-delegated-administrator` command\.

   ```
   aws organizations register-delegated-administrator \
     --service-principal=member.org.stacksets.cloudformation.amazonaws.com \
     --account-id="memberAccountId"
   ```

1. Run the `list-delegated-administrators` command to verify that the specified member account is successfully registered as a delegated administrator\.

   ```
   aws organizations list-delegated-administrators \
     --service-principal=member.org.stacksets.cloudformation.amazonaws.com
   ```

**To deregister a delegated administrator \(AWS CLI\)**

1. Open the AWS CLI\.

1. Run the `deregister-delegated-administrator` command\.

   ```
   aws organizations deregister-delegated-administrator \
     --service-principal=member.org.stacksets.cloudformation.amazonaws.com \
     --account-id="memberAccountId"
   ```

1. Run the `list-delegated-administrators` command to verify that the specified member account is successfully deregistered as a delegated administrator\.

   ```
   aws organizations list-delegated-administrators \
     --service-principal=member.org.stacksets.cloudformation.amazonaws.com
   ```

   You can register this account again at any time\.