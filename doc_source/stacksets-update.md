# Update your stack set<a name="stacksets-update"></a>

You can update your stack set in either the AWS Management Console, or by using AWS CloudFormation commands in the AWS CLI\. In this walkthrough, we are changing the default snapshot delivery frequency for delivery channel configuration from **24hours** to **12hours**\.

To override parameter values for specific stack *instances*, see [Override parameters on stack instances](stackinstances-override.md)\.

**Topics**
+ [Update your stack set using the AWS CloudFormation console](#stacksets-update-console)
+ [Update your stack set using the AWS CLI](#stacksets-update-cli)

## Update your stack set using the AWS CloudFormation console<a name="stacksets-update-console"></a>

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. On the StackSets page, select the stack set that you created in [Create a stack set](stacksets-getting-started-create.md)\. In this walkthrough, we created a stack set named `my-awsconfig-stackset`\.

1. With the stack set selected, choose **Edit StackSet details** from the **Actions** menu\.  
![\[Update stack set in stack set page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-action-edit-stackset.png)

1. On the **Choose a template** page, choose whether you want to update the current template, specify an S3 URL to another template, or upload a new template to AWS CloudFormation\. In this walkthrough, we are using the current template\. Choose **Use current template**, and then choose **Next**\.

1. On the **Specify StackSet details** page, modify parameter values and specify deployment targets\.

   1. \[Self\-managed permissions\] For **Deployment targets**, choose **Deploy stacks in accounts**\. Paste your target account numbers in the text box, separating multiple numbers with commas\. 

      \[Service\-managed permissions\] For **Deployment targets**, choose the accounts in your organization to deploy to\.   
![\[Deploy stack set updates to all accounts in select OUs within your organization.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-update-deployment-targets.png)

   1. Change the value of the **Frequency** parameter from **24hours** to **12hours**\.

      For more information about this and the other parameters, which specify values used by AWS Config, see [Setting up AWS Config with the console](http://docs.aws.amazon.com/config/latest/developerguide/gs-console.html) in the *AWS Config Developer Guide*\.

      Do not make changes to the other parameters\. For the purposes of this walkthrough, we are not configuring Amazon SNS updates\.

      When done, choose **Next**\.

1. On the **Configure StackSet options** page, no changes are needed, but you can update, delete, or add new tags here if desired\. For more information about how tags are used in AWS, see [Using cost allocation tags](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\. 

   Leave the **Permissions** unchanged, and choose **Next**\.

1. On the **Set deployment options** page, keep the default value of **1** and **By number** for **Maximum concurrent accounts**\. Keep the default **Failure tolerance** of **0**, and keep the **By number** default option\. Choose **Next**\.
**Note**  
You cannot change accounts and Regions here; that is, you cannot deploy stack set changes to stacks in some accounts and Regions, but not others\.

1. On the **Review** page, review your choices and your stack set's properties\. To make changes, choose **Edit** in the upper\-right corner of an area in which you want to change properties\. Before you can update the stack set, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are updating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM resources in AWS CloudFormation templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready to create your stack set, choose **Submit**\.

   AWS CloudFormation starts applying your updates to your stack set, and displays the **Operations** tab of the stack set details page 

1. You can view the progress and status of update operations on the **Operations** tab\. You should see the updated **Frequency** parameter in the **Parameter** tab\.

## Update your stack set using the AWS CLI<a name="stacksets-update-cli"></a>

Run the `update-stack-set` AWS CLI command to make changes to your stack set\. In this walkthrough, we are updating the value of the `MaximumExecutionFrequency` parameter\. For more information about the parameter names and values for creating or updating an AWS Config rule, see [put\-config\-rule](http://docs.aws.amazon.com/cli/latest/reference/configservice/put-config-rule.html) in the AWS CLI reference\. To change template parameter values, add the `--parameters` parameter\. For more information about what you can specify as a value for `--parameters`, see [Parameter](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_Parameter.html) in the AWS CloudFormation API Reference, and [http://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html) in the *AWS CLI Command Reference*\.

In the example command shown here, we are updating the stack set by using `--parameters`; specifically, we change the default snapshot delivery frequency for delivery channel configuration from **TwentyFour\_Hours** to **Twelve\_Hours**\. Because we are still using the current template, we add the `--use-previous-template` parameter\.

1. Run the following command\. For *stack set name*, specify the stack set name `my-awsconfig-stackset`\.

   Set the failure tolerance and maximum concurrent accounts by setting `FailureToleranceCount` to `0`, and `MaxConcurrentCount` to `1` in the `--operation-preferences` parameter, as shown in the following example\. To apply percentages instead, use `FailureTolerancePercentage` or `MaxConcurrentPercentage`\. For the purposes of this walkthrough, we are using count, not percentage\.
**Note**  
The value of `MaxConcurrentCount` is dependent on the value of `FailureToleranceCount`\. `MaxConcurrentCount` is at most one more than `FailureToleranceCount`\.

   \[Self\-managed permissions\] Provide the account IDs you want your update to target\.

   ```
   aws cloudformation update-stack-set --stack-set-name my-awsconfig-stackset --use-previous-template --parameters ParameterKey=MaximumExecutionFrequency,ParameterValue=TwentyFour_Hours\\,Twelve_Hours --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1 --accounts 
   ```

   \[Service\-managed permissions\] Provide the organization \(root\) ID, OU IDs, or AWS Organizations account IDs you want your update to target\.

   ```
   aws cloudformation update-stack-set --stack-set-name my-awsconfig-stackset --use-previous-template --parameters ParameterKey=MaximumExecutionFrequency,ParameterValue=TwentyFour_Hours\\,Twelve_Hours --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1 --deployment-targets OrganizationalUnitIds='["ou-rcuk-1x5j1lwo", "ou-rcuk-slr5lh0a"]' --regions '["eu-west-1"]' 
   ```

1. Verify that your stack set was updated successfully by running the `describe-stack-set-operation` command to show the status and results of your update operation\. For `--operation-id`, use the operation ID that was returned by your `update-stack-set` command\.

   ```
   aws cloudformation describe-stack-set-operation --operation-id operation_ID
   ```