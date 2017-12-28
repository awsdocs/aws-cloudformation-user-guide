# Override Parameters on Stack Instances<a name="stackinstances-override"></a>

In certain cases, you might want stack instances in certain regions or accounts to have different property values than those specified in the stack set itself\. For example, you might want to specify a different value for a given parameter based on whether an account is used for development or production\. For these situations, AWS CloudFormation allows you to override parameter values in stack instances by account and region\. You can override template parameter values when you first create the stack instances, and you can override parameter values for existing the stack instances\. You can only set parameters you've previously overridden in stack instances back to the values specified in the stack set\.

Parameter value overrides apply to stack instances in the accounts and regions you select\. During stack set updates, any parameter values overridden for a stack instance are not updated, but retain their overridden value\. 

You can only override parameter *values* that are specified in the stack set; to add or delete a parameter itself, you need to update the stack set template\. If you add a parameter to a stack set template, then before you can override that parameter value in a stack instance you must first update all stack instances with the new parameter and value specified in the stack set\. Once all stack instances have been updated with the new parameter, you can then override the parameter value in individual stack instances as desired\.

To learn how to override stack set parameter values when you create stack instances, see [Add Stacks to a Stack Set](stackinstances-create.md)\.

**To override parameter values in stack instances by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. At the top of the page, choose **StackSets**\. On the StackSets home page, select the stack set that you created in [Create a New Stack Set](stacksets-getting-started-create.md)\. In that walkthrough, we created a stack set named `my-awsconfig-stackset`\.

1. With the stack set selected, choose **Manage stacks in StackSet** from the **Actions** menu\.

1. Choose **Override parameters for selected stacks**, and then choose **Next**

1. On the **Set deployment options** page, in the **Specify accounts** area, choose **Update stacks in account**\.

1. In the **Account** text box, paste some or all target account IDs that you used to create your stack set in [Create a New Stack Set](stacksets-getting-started-create.md)\.

1. In the **Specify regions** area, choose all regions \(hold down **Ctrl** while selecting regions to select multiple regions\), and then choose **Add** to add all stack set regions to the list\. 

1. In the **Deployment options** area, leave the default value of **1** and **By number** for **Maximum concurrent accounts**, and change the value of **Failure tolerance** to **1**\. Be sure **Failure tolerance** is also set to **By number**\. Choose **Next**\.

1. On the **Set overrides** page, in the **Delivery Channel Configuration** section, for the **Snapshot delivery frequency** parameter check **Override existing value** and then select **6hours**\. You are instructing AWS CloudFormation to override the **Snapshot delivery frequency** parameter value and use **6hours** for all the stack instances for the specified accounts in the specified regions\. Choose **Next**\.
**Note**  
To set any overridden parameters back to using the value specified in the stack set, select **Revert all parameters to StackSet values**\. Doing so removes all overridden values once you update the stack instances\.

1. Click **Next**\.

1. On the **Review** page, review your choices\. Note that the **Snapshot delivery frequency** parameter displays an **override** icon, indicating that its value has been overridden at the stack level\.

   Choose **Edit** in the upper right corner of each section to go back and make any changes, if necessary\. When you are ready to update your stacks with the overridden parameter, choose **Update stacks**\.