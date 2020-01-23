# Override Parameters on Stack Instances<a name="stackinstances-override"></a>

In certain cases, you might want stack instances in certain regions or accounts to have different property values than those specified in the stack set itself\. For example, you might want to specify a different value for a given parameter based on whether an account is used for development or production\. For these situations, AWS CloudFormation allows you to override parameter values in stack instances by account and region\. You can override template parameter values when you first create the stack instances, and you can override parameter values for existing stack instances\. You can only set parameters you've previously overridden in stack instances back to the values specified in the stack set\.

Parameter value overrides apply to stack instances in the accounts and regions you select\. During stack set updates, any parameter values overridden for a stack instance are not updated, but retain their overridden value\. 

You can only override parameter *values* that are specified in the stack set; to add or delete a parameter itself, you need to update the stack set template\. If you add a parameter to a stack set template, then before you can override that parameter value in a stack instance you must first update all stack instances with the new parameter and value specified in the stack set\. Once all stack instances have been updated with the new parameter, you can then override the parameter value in individual stack instances as desired\.

To learn how to override stack set parameter values when you create stack instances, see [Add Stacks to a Stack Set](stackinstances-create.md)\.

**To override parameter values in stack instances by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\. On the StackSets page, select the stack set that you created in [Create a New Stack Set](stacksets-getting-started-create.md)\. In that walkthrough, we created a stack set named `my-awsconfig-stackset`\.

1. With the stack set selected, choose **Override StackSet parameters** from the **Actions** menu\.  
![\[Manage stacks in stack set page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-action-override-parameters.png)

1. On the **Set deployment options** page, provide the accounts and regions for the stack instances whose parameters you want to override\. 

   AWS CloudFormation will deploy stacks in the specified accounts within the first region, then moves on to the next, and so on, as long as a region's deployment failures do not exceed a specified failure tolerance\.

   1. For **Accounts**, choose **Deploy stacks in accounts**\. Paste some or all the target account IDs that you used to create your stack set in [Create a New Stack Set](stacksets-getting-started-create.md)\.

   1. For **Specify regions**, add one or more of the regions into which you have deployed stack instances for this stack set\. 

      If you add multiple regions, the order of the regions under **Specify regions** determines their deployment order\.

   1. For **Deployment options**: 
      + For **Maximum concurrent accounts**, keep the default values of **Number** and **1**\.

        This means that AWS CloudFormation deploys your stack in only one account at one time\.
      + For **Failure tolerance**, keep the defauls of **Number** and **0**\.

        This means that a maximum of one stack deployment can fail in one of your specified regions before AWS CloudFormation stops deployment in the current region, and cancels deployment in remaining regions\.

      Choose **Next**\.

1. On the **Specify Overrides** page, check the **Frequency** parameter and then choose **Override StackSet value** from the **Edit override value** menu\.  
![\[Select parameters to override and then select Override StackSet value\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-override-parameters-edit-value.png)

1. In **Override StackSet parameter values**, select **6hours** for the **Frequency** parameter, and choose **Save changes**\. You are instructing AWS CloudFormation to override the **Frequency** parameter value and use **6hours** for all the stack instances for the specified accounts in the specified regions\. Choose **Next**\.
**Note**  
To set any overridden parameters back to using the value specified in the stack set, check all parameters and choose **Set to StackSet value** from the **Edit override value** menu\. Doing so removes all overridden values once you update the stack instances\.

1. On the **Review** page, review your choices\. Note that the **Frequency** parameter displays a value in the **Override value** column, indicating that its value has been overridden at the stack level\.

   Before you can override parameters for these stack instances, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are creating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM Resources in AWS CloudFormation Templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready, choose **Submit**\.

1. AWS CloudFormation starts updating your stack instances\. View the progress and status of the stack instances in the stack set details page that opens when you choose **Submit**\. 