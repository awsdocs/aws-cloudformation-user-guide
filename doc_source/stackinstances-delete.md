# Delete Stack Instances<a name="stackinstances-delete"></a>

You can delete stack instances from a stack set in either the AWS Management Console, or by using AWS CloudFormation commands in the AWS CLI\. In this procedure, we will delete all stacks\.

**To delete stack instances by using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. At the top of the page, choose **StackSets**\. On the StackSets home page, select the stack set that you created in [Create a New Stack Set](stacksets-getting-started-create.md)\. In this walkthrough, we created a stack set named `my-awsconfig-stackset`\.  
![\[Select stack set\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_my_awsconfig.png)

1. With the stack set selected, choose **Manage stacks in stack set** from the **Actions** menu\.

1. Choose **Delete stacks**, and then choose **Next**\.  
![\[Manage stacks in stack set, Delete stacks selected\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_manage_delete.png)

1. On the **Set deployment options** page, in the **Accounts** area, choose **Delete stacks from account**\.  
![\[Delete stacks from all accounts\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_delete_accounts.png)

1. In the **Delete stacks from account** text box, paste all target account IDs that you used to create your stack set in [Create a New Stack Set](stacksets-getting-started-create.md)\.

1. In the **Regions** area, choose all regions \(hold down **Ctrl** while selecting regions to select multiple regions\), and then choose **Add** to add all stack set regions to the list\. You are instructing AWS CloudFormation to delete all stacks, in all target accounts across all regions\.

1. In the **Preferences** area, leave the default value of **1** and **By number** for **Maximum concurrent accounts**, and change the value of **Failure tolerance** to **1**\. Be sure **Failure tolerance** is also set to **By number**\.

1. In the **Retain stacks** area, keep the default setting, **No**\.

   When you are deleting stacks from a stack set, the **Retain stacks** option lets you choose to remove the stack instances from your stack set, but save the stacks and their associated resources\. When you save stacks from a stack set by choosing the **Retain stacks** option, the stack's resources stay in their current state, but the stack is no longer part of the stack set\. You cannot reassociate a retained stack, or add an existing, saved stack to a new stack set\. The stack is permanently independent of a stack set\. In this procedure, we are deleting all stacks in preparation for deleting the entire stack set, so we are not retaining stacks\.

1. Choose **Next**\.

1. On the **Review** page, review your choices\. Choose **Edit** in the upper right corner of each section to go back and make any changes, if necessary\. When you are ready to delete your stacks, choose **Delete stacks**\.

1. After stack deletion is finished, you can verify that stack instances were deleted from your stack set in the StackSets management console, on the home page\.

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