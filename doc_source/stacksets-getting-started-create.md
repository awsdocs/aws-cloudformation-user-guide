# Create a stack set<a name="stacksets-getting-started-create"></a>

You can create a stack set using the AWS Management Console or using AWS CloudFormation commands in the AWS CLI\. You can create a stack set with either `self-managed` or `service-managed` permissions\. 

With `self-managed` permissions, you can deploy stack instances to specific AWS accounts in specific Regions\. To do this, you must first create the necessary IAM roles to establish a trusted relationship between the account you're administering the stack set from and the account you're deploying stack instances to\.

With `service-managed` permissions, you can deploy stack instances to accounts managed by AWS Organizations in specific Regions\. With this model, you don't need to create the necessary IAM roles; StackSets creates the IAM roles on your behalf\. You can also enable automatic deployments to accounts that are added to a target organization or organizational unit \(OU\) in the future\. With automatic deployments enabled, StackSets automatically deletes stack instances from an account if it is removed from a target organization or OU\. 

**Topics**
+ [Create a stack set with self\-managed permissions](#stacksets-getting-started-create-self-managed)
+ [Create a stack set with service\-managed permissions](#stacksets-orgs-associate-stackset-with-org)

## Create a stack set with self\-managed permissions<a name="stacksets-getting-started-create-self-managed"></a>

**Topics**
+ [Create a stack set with self\-managed permissions using the AWS Management Console](#stacksets-getting-started-create-self-managed-console)
+ [Create a stack set with self\-managed permissions using the AWS CLI](#stacksets-getting-started-self-managed-cli)

### Create a stack set with self\-managed permissions using the AWS Management Console<a name="stacksets-getting-started-create-self-managed-console"></a>

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. At the top of the **StackSets** page, choose **Create StackSet**\.

1. Under **Prerequisite \- Prepare template**, choose **Use a sample template**\.

1. Under **Select a sample template**, from the drop\-down menu choose the **Enable AWS config** template\. Click **Next**\.  
![\[StackSets sample Enable AWS Config template\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-choose-template.png)

1. On the **Specify StackSet details** page, provide the following information\.

   1. Provide a name for the stack set\. Stack set names must begin with an alphabetical character, and contain only letters, numbers, and hyphens\. In this walkthrough, we use the name **my\-awsconfig\-stackset**\.

   1. You are prompted to specify values for parameters that are used by AWS Config\. For more information about these parameters, see [Setting up AWS Config with the console](http://docs.aws.amazon.com/config/latest/developerguide/gs-console.html) in the *AWS Config Developer Guide*\. In this walkthrough, we will leave default settings for all AWS Config parameters\.

   1. You can configure Amazon Simple Notification Service \(SNS\) updates by email, based on log content, using the **TopicARN** and **NotificationEmail** parameters\. For the purposes of this walkthrough, we are not configuring Amazon SNS updates\.

   1. You can configure the delivery channel for updates and notifications using the **DeliveryChannelName** and **Frequency** parameters\. For more information about the delivery channel in AWS Config, see [Managing the delivery channel](http://docs.aws.amazon.com/config/latest/developerguide/manage-delivery-channel.html) in the *AWS Config Developer Guide*\. For the purposes of this walkthrough, we are leaving default settings in this area\.

1. When you are finished specifying parameters for AWS Config, choose **Next**\.

1. On the **Configure StackSet options** page, add a tag by specifying a key and value pair\. In this walkthrough, we create a tag called **Stage**, with a value of **Test**\. Tags that you apply to stack sets are applied to all resources that are created by your stacks\. For more information about how tags are used in AWS, see [Using cost allocation tags](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\. 

   Leave **Permissions** unspecified, and choose **Next**\.  
![\[Tags page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-configure-options.png)

1. On the **Set deployment options** page, provide the accounts and Regions into which you want stacks in your stack set deployed\. 

   AWS CloudFormation will deploy stacks in the specified accounts within the first Region, then moves on to the next, and so on, as long as a Region's deployment failures do not exceed a specified failure tolerance\.

   1. For **Accounts**, choose **Deploy stacks in accounts**\. Paste your target account numbers in the text box, separating multiple numbers with commas\.

   1. For **Specify regions**, choose US East \(N\. Virginia\) Region\. Repeat for the US West \(Oregon\) Region\. Click the up arrow next to US West \(Oregon\) Region to move it to be the first entry in the list\. The order of the Regions under **Specify regions** determines their deployment order\.

   1. For **Deployment options**: 
      + For **Maximum concurrent accounts**, keep the default values of **Number** and **1**\.

        This means that AWS CloudFormation deploys your stack in only one account at one time\.
      + For **Failure tolerance**, keep the defaults of **Number** and **0**\.

        This means that a maximum of one stack deployment can fail in one of your specified Regions before AWS CloudFormation stops deployment in the current Region, and cancels deployment in remaining Regions\.

      Choose **Next**\.  
![\[Set Deployment Options page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-set-depoy-options.png)

1. On the **Review** page, review your choices and your stack set's properties\. To make changes, choose **Edit** in the area in which you want to change properties\. Before you can create the stack set, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are creating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM resources in AWS CloudFormation templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready to create your stack set, choose **Submit**\.  
![\[Acknowledge required capabilities\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-review-capabilities.png)

1. AWS CloudFormation starts creating your stack set\. View the progress and status of the creation of the stacks in your stack set in the stack set details page that opens when you choose **Submit**\.  
![\[Operations tab of the StackSets details page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-detail-operations.png)

### Create a stack set with self\-managed permissions using the AWS CLI<a name="stacksets-getting-started-self-managed-cli"></a>

When you create stack sets by using AWS CLI commands, you run two separate commands: `create-stack-set` to upload your template and create the stack set container, and `create-stack-instances` to create the stacks within your stack set\. Start by running an AWS CLI command, `create-stack-set`, to upload the sample AWS CloudFormation template that enables AWS Config, and then start stack set creation\.

1. Open the AWS CLI\.

1. Run the following command\. For the `--template-url` parameter, provide the URL of the Amazon S3 bucket in which you are storing your template\. For this walkthrough, we use `my-awsconfig-stackset` as the value of the `--stack-set-name` parameter\.

   ```
   aws cloudformation create-stack-set --stack-set-name my-awsconfig-stackset --template-url https://s3.amazonaws.com/cloudformation-stackset-sample-templates-us-east-1/EnableAWSConfig.yml
   ```

1. After your `create-stack-set` command is finished, run the `list-stack-sets` command to see that your stack set has been created\. You should see your new stack set in the results\.

   ```
   aws cloudformation list-stack-sets
   ```

1. Run the `create-stack-instances` AWS CLI command to add stack instances to your stack set\. In this walkthrough, we use `us-west-2` and `us-east-1` as the values of the `--regions` parameter\.

   Set the failure tolerance and maximum concurrent accounts by setting `FailureToleranceCount` to `0` and `MaxConcurrentCount` to `1` in the `--operation-preferences` parameter, as shown in the following example\. To apply percentages instead, use `FailureTolerancePercentage` or `MaxConcurrentPercentage`\. For the purposes of this walkthrough, we are using count, not percentage\.
**Note**  
The value of `MaxConcurrentCount` is dependent on the value of `FailureToleranceCount`\. `MaxConcurrentCount` is at most one more than `FailureToleranceCount`\.

   ```
   aws cloudformation create-stack-instances --stack-set-name my-awsconfig-stackset --accounts '["account_ID_1","account_ID_2"]' --regions '["region_1","region_2"]' --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1
   ```
**Note**  
The concurrency of the StackSet instances deployments in the operation is dependent on the value of `FailureToleranceCount-MaxConcurrentCount` and is at most one more than the `FailureToleranceCount`\.
**Important**  
Wait until an operation is complete before starting another one\. You can run only one operation at a time\.

1. Verify that the stack instances were created successfully\. Run `DescribeStackSetOperation` with the `operation-id` that is returned as part of the output of step 4\.

   ```
   aws cloudformation describe-stack-set-operation --stack-set-name my-awsconfig-stackset --operation-id operation_ID
   ```

## Create a stack set with service\-managed permissions<a name="stacksets-orgs-associate-stackset-with-org"></a>

**Topics**
+ [Considerations when creating a stack set with service\-managed permissions](#stacksets-orgs-considerations)
+ [Create a stack set with service\-managed permissions using the AWS CloudFormation console](#stacksets-orgs-associate-stackset-with-org-console)
+ [Create a stack set with service\-managed permissions using the AWS CLI](#stacksets-orgs-associate-stackset-with-org-cli)

### Considerations when creating a stack set with service\-managed permissions<a name="stacksets-orgs-considerations"></a>
+ Your stack set can target your entire organization or specified organizational units \(OUs\)\. If your stack set targets your organization, it also targets all accounts in all OUs in the organization\. If your stack set targets specified OUs, it also targets all accounts in those OUs\.
+ If your stack set targets a parent OU, the stack set also targets any child OUs\.
+ Multiple stack sets can target the same organization or OU\.
+ Your stack set cannot target accounts outside your organization\.
+ Your stack set cannot deploy nested stacks\.
+ StackSets does not deploy stack instances to the organization's management account, even if the management account is in your organization or in an OU in your organization\.
+ Automatic deployment is set at the stack set level\. You cannot adjust automatic deployments selectively for OUs, accounts, or Regions\.
+ The permissions of the IAM principal entity \(user, role, or group\) that you use to sign in to the management account determine whether you are authorized to deploy with StackSets\. For an example IAM policy that grants permissions to deploy to an organization, see [Sample policy that grants service\-managed stack set permissions](using-iam-template.md#resource-level-permissions-service-managed-stack-set)\.

### Create a stack set with service\-managed permissions using the AWS CloudFormation console<a name="stacksets-orgs-associate-stackset-with-org-console"></a>

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation)\.

1. From the navigation pane, choose **StackSets**\.

1. At the top of the **StackSets** page, choose **Create StackSet**\.

1. Under **Prepare template**, choose **Template is ready**\.

1. Under **Specify template**, choose to either specify the URL for the S3 bucket that contains your stack template or upload a stack template file\. Choose **Next**\.

1. On the **Specify StackSet details** page, provide a name for the stack set, specify any parameters, and then choose **Next**\.

1. On the **Configure StackSet options** page, under **Tags**, specify any tags to apply to resources in your stack\.

1. Under **Permissions**, choose **Service\-managed permissions**\.

   If trusted access with AWS Organizations is disabled, a banner displays\. Trusted access is required to create or update a stack set with service\-managed permissions\. Only the administrator in the organization's management account has permissions to [enable trusted access](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-enable-trusted-access.html)\.  
![\[Enable trusted access banner.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-service-managed-permissions.png)

1. Choose **Next** to proceed and to enable trusted access if not already enabled\.

1. On the **Set deployment options** page, under **Deployment targets**, choose the accounts in your organization to deploy to\.
   + Choose **Deploy to organization** to deploy to all accounts in your organization\.  
![\[Deploy stack instances to all accounts in your organization.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-deploy-to-org.png)
   + Choose **Deploy to organizational units \(OUs\)** to deploy to all accounts in specific OUs\. Choose **Add an OU**, and then paste the target OU ID in the text box\. Repeat for each new target OU\.  
![\[Deploy stack instances to all accounts in select OUs within your organization.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-deploy-to-organizational-units.png)

1. Under **Automatic deployment**, choose whether StackSets will automatically deploy to accounts that are added to the target organization or OUs in the future\.  
![\[Automatic deployment settings for stack sets with service-managed permissions.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-auto-deploy.png)

1. If you enabled automatic deployment, under **Account removal behavior**, choose whether stack resources are retained or deleted when an account is removed from a target organization or OU\.  
![\[Account removal behavior settings for stack sets with service-managed permissions.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-account-removal-retain.png)
**Note**  
With **Retain stacks** selected, stack instances are removed from your stack set, but the stacks and their associated resources are retained\. The resources stay in their current state, but will no longer be part of the stack set\. The stacks cannot be reassociated with an existing or new stack set\.

1. Under **Deployment regions**, choose the Regions in which you want to deploy stack instances\. Choose **Next**\.

1. On the **Review** page, verify that StackSets will deploy to the correct accounts in the correct Regions, and then choose **Create StackSet**\.

The **StackSet details** page opens\. You can view the progress and status of the creation of the stacks in your stack set\.

### Create a stack set with service\-managed permissions using the AWS CLI<a name="stacksets-orgs-associate-stackset-with-org-cli"></a>

When you create stack sets using the AWS CLI, you run two separate commands\. During `create-stack-set`, you upload your template, create the stack set container, and manage automatic deployments\. During `create-stack-instances`, you create stack instances in specific target accounts\.

1. Open the AWS CLI\.

1. Run the `create-stack-set` command\. In the following example, we enable automatic deployments to allow StackSets to automatically deploy to accounts that are added to the target organization or OUs in the future\. We also retain stack resources when an account is removed from a target organization or OU\.

   ```
   aws cloudformation create-stack-set --stack-set-name StackSet_myApp --template-url https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/MyApp.template --permission-model SERVICE_MANAGED --auto-deployment Enabled=true,RetainStacksOnAccountRemoval=true
   ```

1. After your `create-stack-set` command is finished, run the `list-stack-sets` command to confirm that your stack set was created\. Your new stack set is listed in the results\.

   ```
   aws cloudformation list-stack-sets
   ```

1. Run the `create-stack-instances` command to add stack instances to your stack set\. For the `--deployment-targets` parameter, specify the organization root ID to deploy to all accounts in your organization, or specify OU IDs to deploy to all accounts in those OUs\. In this example, we specify OUs with `ou-rcuk-1x5j1lwo` and `ou-rcuk-slr5lh0a` IDs\.

   ```
   aws cloudformation create-stack-instances --stack-set-name StackSet_myApp --deployment-targets OrganizationalUnitIds='["ou-rcuk-1x5j1lwo", "ou-rcuk-slr5lh0a"]' --regions '["eu-west-1"]'
   ```
**Important**  
Wait until an operation is complete before starting another one\. You can run only one operation at a time\.

1. Using the `operation-id` that was returned as part of the `create-stack-instances` output in step 4, run `describe-stack-set-operation` to verify that your stack instances were created successfully\.