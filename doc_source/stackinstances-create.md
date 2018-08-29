# Add Stacks to a Stack Set<a name="stackinstances-create"></a>

When you create a stack set, you can create the stacks for that stack set\. AWS CloudFormation also enables you to add more stacks, for additional accounts and regions, at any point after the stack set is created\. You can add stack instances using either the AWS Management Console, or by using AWS CloudFormation commands in the AWS CLI\. In this procedure, we will add stack instances for an additional region to the stack set we created in [Create a New Stack Set](stacksets-getting-started-create.md)\.

**To add stacks to a stack set by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. At the top of the page, choose **StackSets**\. On the StackSets home page, select the stack set that you created in [Create a New Stack Set](stacksets-getting-started-create.md)\. In this walkthrough, we created a stack set named `my-awsconfig-stackset`\.

1. With the stack set selected, choose **Manage stacks in stack set** from the **Actions** menu\.

1. Choose **Create stacks**, and then choose **Next**\.

1. On the **Set deployment options** page, in the **Accounts** area, choose **Create stacks from account**\.

1. In the **Create stacks from account** text box, paste all target account IDs that you used to create your stack set in [Create a New Stack Set](stacksets-getting-started-create.md)\.

1. In the **Regions** area, choose US West \(N\. California\), and then choose **Add**\. You will be creating new stacks, in the US West \(N\. California\) region, for the accounts you've specified\.

1. In the **Preferences** area, leave the default value of **1** and **By number** for **Maximum concurrent accounts**, and change the value of **Failure tolerance** to **1**\. Be sure **Failure tolerance** is also set to **By number**\. Choose **Next**\.

1. On the **Set overrides** page, leave the property values as specified\. You won't be overriding any property values for the stacks you're going to create\. Choose **Next**\.

1. On the **Review** page, review your choices and your stacks' properties\. To make changes, choose **Edit** in the area in which you want to change properties\. When you are are ready to create your stacks, choose **Create stacks**\.

1. AWS CloudFormation starts creating your stacks\. View the progress and status of the creation of the stacks in your stack set in the **Properties** page that opens when you choose **Create stacks**\.