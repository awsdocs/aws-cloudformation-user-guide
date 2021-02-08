# Override parameters on stack instances<a name="stackinstances-override"></a>

In certain cases, you might want stack instances in certain Regions or accounts to have different property values than those specified in the stack set itself\. For example, you might want to specify a different value for a given parameter based on whether an account is used for development or production\. For these situations, AWS CloudFormation allows you to override parameter values in stack instances by account and Region\. You can override template parameter values when you first create the stack instances, and you can override parameter values for existing stack instances\. You can only set parameters you've previously overridden in stack instances back to the values specified in the stack set\.

Parameter value overrides apply to stack instances in the accounts and Regions you select\. During stack set updates, any parameter values overridden for a stack instance are not updated, but retain their overridden value\. 

You can only override parameter *values* that are specified in the stack set; to add or delete a parameter itself, you need to update the stack set template\. If you add a parameter to a stack set template, then before you can override that parameter value in a stack instance you must first update all stack instances with the new parameter and value specified in the stack set\. Once all stack instances have been updated with the new parameter, you can then override the parameter value in individual stack instances as desired\.

To learn how to override stack set parameter values when you create stack instances, see [Add stacks to a stack set](stackinstances-create.md)\.

**Topics**
+ [Override parameters on stack instances using the AWS Management Console](#stackinstances-override-console)
+ [Override parameters on stack instances using the AWS CLI](#stackinstances-override-cli)

## Override parameters on stack instances using the AWS Management Console<a name="stackinstances-override-console"></a>

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\. On the StackSets page, select the stack set that you created in [Create a stack set](stacksets-getting-started-create.md)\. In that walkthrough, we created a stack set named `my-awsconfig-stackset`\.

1. With the stack set selected, choose **Override StackSet parameters** from the **Actions** menu\.  
![\[Manage stacks in stack set page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-action-override-parameters.png)

1. On the **Set deployment options** page, provide the accounts and Regions for the stack instances whose parameters you want to override\. 

   AWS CloudFormation will deploy stacks in the specified accounts within the first Region, then moves on to the next, and so on, as long as a Region's deployment failures do not exceed a specified failure tolerance\.

   1. \[Self\-managed permissions\] For **Deployment targets**, choose **Deploy stacks in accounts**\. Paste some or all the target account IDs that you used to create your stack set in [Create a stack set](stacksets-getting-started-create.md)\.

      \[Service\-managed permissions\] For **Deployment targets**, choose the accounts in your organization to deploy to\. 
      + Choose **Deploy to organizational units \(OUs\)**\. Select one or more of the target OUs that you used to create your stack set in [Create a stack set](stacksets-getting-started-create.md)\. The overridden parameter values only apply to the accounts that are currently in the target OUs and their child OUs\. Accounts added to the target OUs and their child OUs in the future will use the stack set default values and not the overridden values\.  
![\[Deploy parameter overrides to all accounts in select OUs within your organization.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-deploy-param-overrides-to-ous.png)
      + Choose **Deploy to accounts**\. Paste some or all of the target OU IDs or account IDs that you used to create your stack set in [Create a stack set](stacksets-getting-started-create.md)\.  
![\[Deploy parameter overrides to select accounts in your organization.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-deploy-param-overrides-to-accounts.png)

   1. For **Deployment regions**, add one or more of the Regions into which you have deployed stack instances for this stack set\. 

      If you add multiple Regions, the order of the Regions under **Specify regions** determines their deployment order\.

   1. For **Deployment options**: 
      + For **Maximum concurrent accounts**, keep the default values of **Number** and **1**\.

        This means that AWS CloudFormation deploys your stack in only one account at one time\.
      + For **Failure tolerance**, keep the defaults of **Number** and **0**\.

        This means that a maximum of one stack deployment can fail in one of your specified Regions before AWS CloudFormation stops deployment in the current Region, and cancels deployment in remaining Regions\.

      Choose **Next**\.

1. On the **Specify Overrides** page, check the **Frequency** parameter and then choose **Override StackSet value** from the **Edit override value** menu\.  
![\[Select parameters to override and then select Override StackSet value\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-override-parameters-edit-value.png)

1. In **Override StackSet parameter values**, select **6hours** for the **Frequency** parameter, and choose **Save changes**\. You are instructing AWS CloudFormation to override the **Frequency** parameter value and use **6hours** for all the stack instances for the specified accounts in the specified Regions\. Choose **Next**\.
**Note**  
To set any overridden parameters back to using the value specified in the stack set, check all parameters and choose **Set to StackSet value** from the **Edit override value** menu\. Doing so removes all overridden values once you update the stack instances\.

1. On the **Review** page, review your choices\. Note that the **Frequency** parameter displays a value in the **Override value** column, indicating that its value has been overridden at the stack level\.

   Before you can override parameters for these stack instances, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are creating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM resources in AWS CloudFormation templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready, choose **Submit**\.

1. AWS CloudFormation starts updating your stack instances\. View the progress and status of the stack instances in the stack set details page that opens when you choose **Submit**\. 

## Override parameters on stack instances using the AWS CLI<a name="stackinstances-override-cli"></a>

Run the `update-stack-instances` AWS CLI command, specifying `--parameter-overrides`\. For more information about specifying `--parameter-overrides`, see [Parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_Parameter.html) in the AWS CloudFormation API Reference, and [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack-instances.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack-instances.html) in the *AWS CLI Command Reference*\.

In the example command shown here, we change the default snapshot delivery frequency for delivery channel configuration from **TwentyFour\_Hours** to **Twelve\_Hours** for the specified stack instances\.

1. Run the following command\. For `--stack-set-name`, specify the stack set name *my\-awsconfig\-stackset*\.

   Set the failure tolerance and maximum concurrent accounts by setting `FailureToleranceCount` to `0`, and `MaxConcurrentCount` to `1` in the `--operation-preferences` parameter, as shown in the following example\. To apply percentages instead, use `FailureTolerancePercentage` or `MaxConcurrentPercentage`\. For this walkthrough, we are using count, not percentage\.
**Note**  
The value of `MaxConcurrentCount` is dependent on the value of `FailureToleranceCount`\. `MaxConcurrentCount` is at most one more than `FailureToleranceCount`\.

   \[Self\-managed permissions\] Provide the account IDs for which you want to override parameter values on stack instances\.

   ```
   aws cloudformation update-stack-instances --stack-set-name my-awsconfig-stackset --parameter-overrides ParameterKey=MaximumExecutionFrequency,ParameterValue=TwentyFour_Hours\\,Twelve_Hours --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1 --accounts '["012345678901"]' --regions '["eu-west-1", "us-west-2"]'
   ```

   \[Service\-managed permissions\] Provide the organization root ID, OU IDs, or AWS Organizations account IDs for which you want to override parameters on stack instances\. In this example, we override parameter values for stack instances in all accounts in the OU with the *ou\-rcuk\-1x5j1lwo* ID\.

   The overridden parameter values only apply to the accounts that are currently in the target OU and its child OUs\. Accounts added to the target OU and its child OUs in the future will use the stack set default values and not the overridden values\.

   ```
   aws cloudformation update-stack-instances --stack-set-name my-awsconfig-stackset --parameter-overrides ParameterKey=MaximumExecutionFrequency,ParameterValue=TwentyFour_Hours\\,Twelve_Hours --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1 --deployment-targets OrganizationalUnitIds='["ou-rcuk-1x5j1lwo"]' --regions '["eu-west-1", "us-west-2"]'
   ```

1. Verify that your parameter values were successfully overidden on stack instances by running the `describe-stack-set-operation` command to show the status and results of your update operation\. For `--operation-id`, use the operation ID that was returned by your `update-stack-instances` command\.

   ```
   aws cloudformation describe-stack-set-operation --operation-id operation_ID
   ```