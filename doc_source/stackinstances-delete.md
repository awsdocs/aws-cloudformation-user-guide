# Delete stack instances from your stack set<a name="stackinstances-delete"></a>

You can delete stack instances from a stack set in either the AWS Management Console, or by using AWS CloudFormation commands in the AWS CLI\. In this procedure, we will delete all stacks\.

For a stack set with service\-managed permissions, if you delete stack instances from a top\-level organizational unit \(OU\), the OU is removed as a target of the stack set\.

**Topics**
+ [Delete stack instances using the AWS Management Console](#stackinstances-delete-console)
+ [Delete stack instances using the AWS CLI](#stackinstances-delete-cli)

## Delete stack instances using the AWS Management Console<a name="stackinstances-delete-console"></a>

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. Choose **StackSets** from the navigation pane\. On the StackSets page, select the stack set that you created in [Create a stack set](stacksets-getting-started-create.md)\.

1. With the stack set selected, choose **Delete stacks from StackSet** from the **Actions** menu\.  
![\[Choose Delete stacks from StackSet from the Actions menu.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacksets-action-delete-stacks.png)

1. On the **Set deployment options** page, choose the accounts from which to delete stack instances\.

   1. \[Self\-managed permissions\] For **Accounts**, choose **Deploy stacks in accounts**\. Paste your target account numbers in the text box, separating multiple numbers with commas\.

      \[Service\-managed permissions\] For **Accounts**, choose **Deploy stacks in organizational units**\. Paste the IDs of the OUs that your stack set targets\.
**Note**  
StackSets also deletes stack instances from any child OUs of the specified target OUs\.  
![\[Select the organizational units from which to delete stack instances.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-delete-stack-instances-in-ous.png)

   1. For **Deployment regions**, choose the Regions from which you want to delete stack instances\. In this case, US East \(N\. Virginia\) Region and US West \(Oregon\) Region\.

   1. For **Deployment options**: 
      + For **Maximum concurrent accounts**, keep the default values of **Number** and **1**\.
      + For **Failure tolerance**, keep the defaults of **Number** and **0**\.

      In the **Retain stacks** area, keep the default setting of disabled\.

      When you are deleting stacks from a stack set, the **Retain stacks** option lets you choose to remove the stack instances from your stack set, but save the stacks and their associated resources\. When you save stacks from a stack set by choosing the **Retain stacks** option, the stack's resources stay in their current state, but the stack is no longer part of the stack set\. You cannot reassociate a retained stack, or add an existing, saved stack to a new stack set\. The stack is permanently independent of a stack set\. In this procedure, we are deleting all stacks in preparation for deleting the entire stack set, so we are not retaining stacks\.

      Choose **Next**\.

1. On the **Review** page, review your choices and choose **Submit**\.

1. After stack deletion is finished, you can verify that stack instances were deleted from your stack set in the StackSet detail page, on the **Stack instances** tab\.  
![\[Use the Stack instances tab of the stack set details page to view information on your stack instances.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-detail-stack-instances.png)

## Delete stack instances using the AWS CLI<a name="stackinstances-delete-cli"></a>

1. Run the `delete-stack-instances` command\. For `--stack-set-name`, specify the stack set name `my-awsconfig-stackset`\.

   Set the failure tolerance and maximum concurrent accounts by setting `FailureToleranceCount` to `0`, and `MaxConcurrentCount` to `1` in the `--operation-preferences` parameter, as shown in the following example\. To apply percentages instead, use `FailureTolerancePercentage` or `MaxConcurrentPercentage`\. For the purposes of this walkthrough, we are using count, not percentage\.
**Note**  
The value of `MaxConcurrentCount` is dependent on the value of `FailureToleranceCount`\. `MaxConcurrentCount` is at most one more than `FailureToleranceCount`\.

   Because `--retain-stacks` is a required parameter of `delete-stack-instances`, if you do not want to retain \(save\) stacks, add `--no-retain-stacks`\. In this walkthrough, we add the `--no-retain-stacks` parameter, because we are not retaining any stacks\.

   \[Self\-managed permissions\] Replace *account\_ID* with the accounts you used to create your stack set in [Create a stack set](stacksets-getting-started-create.md)\.

   ```
   aws cloudformation delete-stack-instances --stack-set-name my-awsconfig-stackset --accounts '["0123456789012"]' --regions '["eu-west-1"]' --operation-preferences FailureToleranceCount=0,MaxConcurrentCount=1 --no-retain-stacks
   ```

   \[Service\-managed permissions\] For `--deployment-targets`, specify the organization \(root\) ID or OU IDs in which you created stack instances\.
**Note**  
StackSets also deletes stack instances from any child OUs of the specified target OUs\.

   ```
   aws cloudformation delete-stack-instances --stack-set-name my-awsconfig-stackset --deployment-targets OrganizationalUnitIds='["ou-rcuk-1x5jlwo", "ou-rcuk-slr5lh0a"]' --regions '["eu-west-1"]' --no-retain-stacks
   ```

1. Optionally, after stack deletion is finished, verify that stack instances were deleted from your stack set by running the `describe-stack-set-operation` command to show the status and results of the delete stacks operation\. For `--operation-id`, use the operation ID that was returned by your `delete-stack-instances` command\.

   ```
   aws cloudformation describe-stack-set-operation --stack-set-name stackSetName --operation-id ddf16f54-ad62-4d9b-b0ab-3ed8e9example
   ```