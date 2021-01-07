# Troubleshooting AWS CloudFormation StackSets<a name="stacksets-troubleshooting"></a>

This topic contains some common AWS CloudFormation StackSets issues, and suggested solutions for those issues\.

**Topics**
+ [Common reasons for stack operation failure](#w7739ab1c29c27b6)
+ [Retrying failed stack creation or update operations](#w7739ab1c29c27b8)
+ [Stack instance deletion fails](#stack-instance-delete-fails)

## Common reasons for stack operation failure<a name="w7739ab1c29c27b6"></a>

**Problem:** A stack operation failed, and the stack instance status is `OUTDATED`\.

**Cause:** There can be several common causes for stack operation failure\.
+ Insufficient permissions in a target account for creating resources that are specified in your template\.
+ The AWS CloudFormation template might have errors\. Validate the template in AWS CloudFormation and fix errors before trying to create your stack set\.
+ The template could be trying to create global resources that must be unique but aren't, such as S3 buckets\.
+ A specified target account number doesn't exist\. Check the target account numbers that you specified on the **Set deployment options** page of the wizard\.
+ The administrator account does not have a trust relationship with the target account\.
+ The maximum number of a resource that is specified in your template already exists in your target account\. For example, you might have reached the limit of allowed IAM roles in a target account, but the template creates more IAM roles\.
+ You have reached the maximum number of stacks that are allowed in a stack set\. See [AWS CloudFormation limits](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html) for the maximum number of stacks per stack set\.

**Solution:** For more information about the permissions required of target and administrator accounts before you can create stack sets, see [Set up basic permissions for stack set operations](stacksets-prereqs-self-managed.md#stacksets-prereqs-accountsetup)\.

## Retrying failed stack creation or update operations<a name="w7739ab1c29c27b8"></a>

**Problem:** A stack creation or update failed, and the stack instance status is `OUTDATED`\. To troubleshoot why a stack creation or update failed, open the AWS CloudFormation console, and view the events for the stack, which will have a status of `DELETED` \(for failed create operations\) or `FAILED` \(for failed update operations\)\. Browse the stack events, and find the **Status reason** column\. The value of **Status reason** explains why the stack operation failed\.

After you have fixed the underlying cause of the stack creation failure, and you are ready to retry stack creation, perform the following steps\.

**Solution:** Perform the following steps to retry your stack operation\.

1. In the console, select the stack set that contains the stack on which the operation failed\.

1. In the **Actions** menu, choose **Edit StackSet details** to retry creating or updating stacks\.

1. On the **Specify template** page, to use the same AWS CloudFormation template, keep the default option, **Use current template**\. If your stack operation failed because the template required changes, and you want to upload a revised template, choose **Upload a template to Amazon S3** instead, and then choose **Browse** to select your updated template\. When you are finished uploading your revised template, choose **Next**\.

1. On the **Specify details** page, if you are not changing any parameters that are specific to your template, choose **Next**\.

1. On the **Set deployment options** page, change defaults for **Maximum concurrent accounts** and **Failure tolerance**, if desired\. For more information about these settings, see [Stack set operation options](stacksets-concepts.md#stackset-ops-options)\.

1. On the **Review** page, review your selections, and fill the checkbox to acknowledge required IAM capabilities\. Choose **Submit**\.

1. If your stack is not successfully updated, repeat this procedure, after you've resolved any underlying issues that are preventing stack creation\.

## Stack instance deletion fails<a name="stack-instance-delete-fails"></a>

**Problem:** A stack deletion has failed\.

**Cause:** Stack deletion will fail for any stacks on which termination protection has been enabled\. 

**Solution:** Determine if termination protection has been enabled for the stack\. If it has, disable termination protection and then perform the stack instance deletion again\.