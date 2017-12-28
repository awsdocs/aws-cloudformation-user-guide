# Update Your Stack Set<a name="stacksets-update"></a>

You can update your stack set in either the AWS Management Console, or by using AWS CloudFormation commands in the AWS CLI\. In this walkthrough, we are changing the default snapshot delivery frequency for delivery channel configuration from **24hours** to **12hours**\.

To override parameter values for specific stack *instances*, see [Override Parameters on Stack Instances](stackinstances-override.md)\.

**To update a stack set by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. At the top of the page, choose **StackSets**\.

1. On the StackSets home page, select the stack set that you created in [Create a New Stack Set](stacksets-getting-started-create.md)\. In this walkthrough, we created a stack set named `my-awsconfig-stackset`\.

1. With the stack set selected, choose **Manage stacks in stack set** from the **Actions** menu\.

1. Choose **Edit stacks**, and then choose **Next**\.  
![\[Manage stacks in stack set page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stackset_edit_stacks.png)

1. On the **Select template** page, choose whether you want to update the current template, specify an S3 URL to another template, or upload a new template to AWS CloudFormation\. In this walkthrough, we are using the current template\. Choose **Current template: Update my\-aws\-config\-stackset**, and then choose **Next**\.  
![\[Select template page\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stackset_current_template.png)

1. On the **Specify details** page of the wizard, change the following information\.

   1. You are prompted to specify values for parameters that are used by AWS Config\. For more information about these parameters, see [Setting up AWS Config with the Console](http://docs.aws.amazon.com/config/latest/developerguide/gs-console.html) in the *AWS Config Developer Guide*\. In this walkthrough, we change the default snapshot delivery frequency for delivery channel configuration from **24hours** to **12hours**\.  
![\[Change AWS Config parameter\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stackset_parameter_change.png)

   1. Do not make changes to the other parameters\. For the purposes of this walkthrough, we are not configuring Amazon SNS updates\.

1. When you are finished updating the **Delivery snapshot frequency** parameter for AWS Config, choose **Next**\.

1. On the **Set deployment options** page, keep the default value of **1** and **By number** for **Maximum concurrent accounts**\. This means that AWS CloudFormation updates your stack in only one account at one time\. Keep the default **Failure tolerance** of **0**, and keep the **By number** default option\. This means that a maximum of one stack update can fail in one of your specified regions before AWS CloudFormation stops updates in the current region, and cancels updates in remaining regions\. Choose **Next**\.
**Note**  
You cannot change accounts and regions here; that is, you cannot deploy stack set changes to stacks in some accounts and regions, but not others\.  
![\[Set update options\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stackset_update_dep_options.png)

1. On the **Tags** page, no changes are needed, but you can update, delete, or add new tags here if desired\. For more information about how tags are used in AWS, see [Using Cost Allocation Tags](http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\. Choose **Next**\.

1. On the **Review** page, review your choices and your stack set's properties\. To make changes, choose **Edit** in the upper\-right corner of an area in which you want to change properties\. Before you can update the stack set, you must fill the check box in the **Capabilities** area to acknowledge that some of the resources that you are updating with the stack set might require new IAM resources and permissions\. For more information about potentially required permissions, see [Acknowledging IAM Resources in AWS CloudFormation Templates](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html#using-iam-capabilities) in this guide\. When you are are ready to create your stack set, choose **Update stacks**\.  
![\[Review update options\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stackset_review_updates.png)

1. AWS CloudFormation starts applying your updates to your stack set\. You can view the progress and status of updates on the stack set properties page that opens after you choose **Update stacks**\. You should see the updated **Delivery snapshot frequency** period in the AWS Config parameters\.

**To update a stack set template by using the AWS CLI**

Run the `update-stack-set` AWS CLI command to make changes to your stack set\. In this walkthrough, we are updating the value of the `MaximumExecutionFrequency` parameter\. For more information about the parameter names and values for creating or updating an AWS Config rule, see [put\-config\-rule](http://docs.aws.amazon.com/cli/latest/reference/configservice/put-config-rule.html) in the AWS CLI reference\. To change template parameter values, add the `--parameters` parameter\. For more information about what you can specify as a value for `--parameters`, see [Parameter](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_Parameter.html) in the AWS CloudFormation API Reference, and [http://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html) in the *AWS CLI Command Reference*\.

In the example command shown here, we are updating the stack set by using `--parameters`; specifically, we change the default snapshot delivery frequency for delivery channel configuration from **TwentyFour\_Hours** to **Twelve\_Hours**\. Because we are still using the current template, we add the `--use-previous-template` parameter\.

1. Run the following command\. For *stack set name*, specify the stack set name `my-awsconfig-stackset`\.

   Set the failure tolerance and maximum concurrent accounts by setting `FailureToleranceCount` to `0`, and `MaxConcurrentCount` to `1` in the `--operation-preferences` parameter, as shown in the following example\. To apply percentages instead, use `FailureTolerancePercentage` or `MaxConcurrentPercentage`\. For the purposes of this walkthrough, we are using count, not percentage\.

   ```
   aws cloudformation update-stack-set --stack-set-name my-awsconfig-stackset --use-previous-template --parameters ParameterKey=MaximumExecutionFrequency,ParameterValue=TwentyFour_Hours\\,Twelve_Hours --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1
   ```

1. Verify that your stack set was updated successfully by running the `describe-stack-set-operation` command to show the status and results of your update operation\. For `--operation-id`, use the operation ID that was returned by your `update-stack-set` command\.

   ```
   aws cloudformation describe-stack-set-operation --operation-id operation_ID
   ```