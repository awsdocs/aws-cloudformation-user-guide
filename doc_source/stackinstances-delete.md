# Delete Stack Instances<a name="stackinstances-delete"></a>

You can delete stack instances from a stack set in either the AWS Management Console, or by using AWS CloudFormation commands in the AWS CLI\. In this procedure, we will delete all stacks\.

**To delete stack instances by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. Choose **StackSets** from the navigation pane\. On the StackSets page, select the stack set that you created in [Create a New Stack Set](stacksets-getting-started-create.md)\. In this walkthrough, we created a stack set named `my-awsconfig-stackset`\.

1. With the stack set selected, choose **Delete stacks from StackSet** from the **Actions** menu\.  
![\[Select stack set and choose Delete stacks from stack set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-action-delete-stacks.png)

1. On the **Set deployment options** page: 

   1. For **Accounts**, choose **Deploy stacks in accounts**\. Paste your target account numbers in the text box, separating multiple numbers with commas\.

   1. For **Specify regions**, choose the regions from which you want to delete stack instances\. In this case, US East \(N\. Virginia\) Region and US West \(Oregon\) Region\.

   1. For **Deployment options**: 
      + For **Maximum concurrent accounts**, keep the default values of **Number** and **1**\.
      + For **Failure tolerance**, keep the defauls of **Number** and **0**\.

      In the **Retain stacks** area, keep the default setting of disabled\.

      When you are deleting stacks from a stack set, the **Retain stacks** option lets you choose to remove the stack instances from your stack set, but save the stacks and their associated resources\. When you save stacks from a stack set by choosing the **Retain stacks** option, the stack's resources stay in their current state, but the stack is no longer part of the stack set\. You cannot reassociate a retained stack, or add an existing, saved stack to a new stack set\. The stack is permanently independent of a stack set\. In this procedure, we are deleting all stacks in preparation for deleting the entire stack set, so we are not retaining stacks\.

      Choose **Next**\.

1. On the **Review** page, review your choices and choose **Submit**\.

1. After stack deletion is finished, you can verify that stack instances were deleted from your stack set in the StackSet detail page, on the **Stack instances** tab\.  
![\[Use the Stack instances tab of the stack set details page to view information on your stack instances.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-detail-stack-instances.png)

**To delete stack instances by using the AWS CLI**

When you are ready to delete stack instances, run the `delete-stack-instances` AWS CLI command\.
+ Run the following command, and replace *account\_ID* with the accounts you used to create your stack set in [Create a New Stack Set](stacksets-getting-started-create.md)\. For *stack set name*, specify the stack set name `my-awsconfig-stackset`\.

  Set the failure tolerance and maximum concurrent accounts by setting `FailureToleranceCount` to `0`, and `MaxConcurrentCount` to `1` in the `--operation-preferences` parameter, as shown in the following example\. To apply percentages instead, use `FailureTolerancePercentage` or `MaxConcurrentPercentage`\. For the purposes of this walkthrough, we are using count, not percentage\.

  Because `--retain-stacks` is a required parameter of `delete-stack-instances`, if you do not want to retain \(save\) stacks, add `--no-retain-stacks`\. In this walkthrough, we add the `--no-retain-stacks` parameter, because we are not retaining any stacks\.

  ```
  aws cloudformation delete-stack-instances --stack-set-name my-awsconfig-stackset --accounts '["account_ID_1","account_ID_2"]' --regions '["region_1","region_2"]' --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1 --no-retain-stacks
  ```

  After stack deletion is finished, you can verify that stack instances were deleted from your stack set by running the `describe-stack-set-operation` command to show the status and results of the delete stacks operation\. For `--operation-id`, use the operation ID that was returned by your `delete-stack-instances` command\.

  ```
  aws cloudformation describe-stack-set-operation --operation-id operation_ID
  ```