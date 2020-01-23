# Add Stacks to a Stack Set<a name="stackinstances-create"></a>

When you create a stack set, you can create the stacks for that stack set\. AWS CloudFormation also enables you to add more stacks, for additional accounts and regions, at any point after the stack set is created\. You can add stack instances using either the AWS CloudFormation console, or by using AWS CloudFormation commands in the AWS CLI\. In this procedure, we will add stack instances for an additional region to the stack set we created in [Create a New Stack Set](stacksets-getting-started-create.md)\.

**To add stacks to a stack set by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\. On the StackSets page, select the stack set that you created in [Create a New Stack Set](stacksets-getting-started-create.md)\. In this walkthrough, we created a stack set named `my-awsconfig-stackset`\.

1. With the stack set selected, choose **Add new stacks to StackSet** from the **Actions** menu\.  
![\[Manage stacks in stack set page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-action-add-stacks.png)

1. On the **Set deployment options** page, provide the accounts and regions into which you want to add stacks for your stack set\. 

   AWS CloudFormation will deploy stacks in the specified accounts within the first region, then moves on to the next, and so on, as long as a region's deployment failures do not exceed a specified failure tolerance\.

   1. For **Accounts**, choose **Deploy stacks in accounts**\. Paste your target account numbers in the text box, separating multiple numbers with commas\.

   1. For **Specify regions**, choose US West \(N\. California\)\. You will be creating new stacks, in the US West \(N\. California\) region, for the accounts you've specified\.

      If you add multiple regions, the order of the regions under **Specify regions** determines their deployment order\.

   1. For **Deployment options**: 
      + For **Maximum concurrent accounts**, keep the default values of **Number** and **1**\.

        This means that AWS CloudFormation deploys your stack in only one account at one time\.
      + For **Failure tolerance**, keep the defauls of **Number** and **0**\.

        This means that a maximum of one stack deployment can fail in one of your specified regions before AWS CloudFormation stops deployment in the current region, and cancels deployment in remaining regions\.

      Choose **Next**\.

1. On the **Specify Overrides** page, leave the property values as specified\. You won't be overriding any property values for the stacks you're going to create\. Choose **Next**\.

1. On the **Review** page, review your choices and your stack set's properties\. To make changes, choose **Edit** in the area in which you want to change properties\. Before you can create the new stacks, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are creating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM Resources in AWS CloudFormation Templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready to create your stack instances, choose **Submit**\.  
![\[Acknowledge required capabilities\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stackset-review-capabilities.png)

1. AWS CloudFormation starts creating your stack instances\. View the progress and status of the creation of the stack instances in your stack set in the stack set details page that opens when you choose **Submit**\. When complete, your new stack instances should be listed on the **Stack instances** tab\.  
![\[Operations tab of the StackSets details page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-detail-operations.png)