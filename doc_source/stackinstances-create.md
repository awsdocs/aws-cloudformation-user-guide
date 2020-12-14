# Add stacks to a stack set<a name="stackinstances-create"></a>

When you create a stack set, you can create the stacks for that stack set\. AWS CloudFormation also enables you to add more stacks, for additional accounts and Regions, at any point after the stack set is created\. You can add stack instances using either the AWS CloudFormation console, or by using AWS CloudFormation commands in the AWS CLI\. In this procedure, we will add stack instances for an additional Region to the stack set we created in [Create a stack set](stacksets-getting-started-create.md)\.

**Topics**
+ [Add stack instances to your stack set using the AWS Management Console](#stackinstances-create-console)
+ [Add stack instances to your stack set using the AWS CLI](#stackinstances-create-cli)

## Add stack instances to your stack set using the AWS Management Console<a name="stackinstances-create-console"></a>

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\. On the StackSets page, select the stack set that you created in [Create a stack set](stacksets-getting-started-create.md)\.

1. With the stack set selected, choose **Add new stacks to StackSet** from the **Actions** menu\.  
![\[Manage stacks in stack set page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-action-add-stacks.png)

1. On the **Set deployment options** page, provide the accounts and Regions into which you want to add stacks for your stack set\.

   AWS CloudFormation will deploy stacks in the specified accounts within the first Region, then moves on to the next, and so on, as long as a Region's deployment failures do not exceed a specified failure tolerance\.

   1. \[Self\-managed permissions\] For **Deployment targets**, choose **Deploy stacks in accounts**\. Paste your target account numbers in the text box, separating multiple numbers with commas\.

      \[Service\-managed permissions\] For **Deployment targets**, choose the accounts in your organization to deploy to\.
      + Choose **Deploy to organization** to deploy to all accounts in your organization\.  
![\[Deploy stack instances to all accounts in your organization.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-deploy-to-org.png)
      + Choose **Deploy to organizational units \(OUs\)** to deploy to all accounts in specific OUs\. Choose **Add another OU**, and then paste the target OU ID in the text box\. Repeat for each new target OU\. StackSets also targets any child OUs of your selected targets\.  
![\[Deploy stack instances to all accounts in select OUs within your organization.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-deploy-to-organizational-units.png)
**Note**  
If you add an OU that your stack set already targets, StackSets creates new stack instances in any accounts in the OU that don't already have stack instances from your stack set \(for example, accounts that were added to the OU after your stack set was created and with automatic deployments disabled\)\.

   1. For **Deployment regions**, choose US West \(N\. California\)\. You will be creating new stacks, in the US West \(N\. California\) Region, for the targets you've specified\.

      If you add multiple Regions, the order of the Regions under **Specify regions** determines their deployment order\.

   1. For **Deployment options**: 
      + For **Maximum concurrent accounts**, keep the default values of **Number** and **1**\.

        This means that AWS CloudFormation deploys your stack in only one account at one time\.
      + For **Failure tolerance**, keep the defaults of **Number** and **0**\.

        This means that a maximum of one stack deployment can fail in one of your specified Regions before AWS CloudFormation stops deployment in the current Region, and cancels deployment in remaining Regions\. If you want CloudFormation to be more failure tolerant, increase this value\.

      Choose **Next**\.

1. On the **Specify Overrides** page, leave the property values as specified\. You won't be overriding any property values for the stacks you're going to create\. Choose **Next**\.

1. On the **Review** page, review your choices and your stack set's properties\. To make changes, choose **Edit** in the area in which you want to change properties\. Before you can create the new stacks, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are creating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM resources in AWS CloudFormation templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready to create your stack instances, choose **Submit**\.  
![\[Acknowledge required capabilities\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-review-capabilities.png)

1. AWS CloudFormation starts creating your stack instances\. View the progress and status of the creation of the stack instances in your stack set in the stack set details page that opens when you choose **Submit**\. When complete, your new stack instances should be listed on the **Stack instances** tab\.  
![\[Operations tab of the StackSets details page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-detail-operations.png)

## Add stack instances to your stack set using the AWS CLI<a name="stackinstances-create-cli"></a>

1. Open the AWS CLI\.

1. Run the `create-stack-instances` command\.

   \[Self\-managed permissions\] Provide the accounts IDs for which you want to create stack instances\.

   ```
   aws cloudformation create-stack-instances --stack-set-name my-awsconfig-stackset --accounts '["account_id"]' --regions '["eu-west-1", "us-west-2"]'
   ```

   \[Service\-managed permissions\] Provide the organization \(root\) ID or OU IDs for which you want to create stack instances\. In this example, we specify OUs with `ou-rcuk-1x5j1lwo` and `ou-rcuk-slr5lh0a` IDs\.

   ```
   aws cloudformation create-stack-instances --stack-set-name StackSet-myApp --deployment-targets OrganizationalUnitIds='["ou-rcuk-r1qi0wl7"]' --regions '["eu-west-1", "us-west-2"]'
   ```
**Note**  
If you add an OU that your stack set already targets, StackSets creates new stack instances in any accounts in the OU that don't already have stack instances from your stack set \(for example, accounts that were added to the OU after your stack set was created and with automatic deployments disabled\)\.