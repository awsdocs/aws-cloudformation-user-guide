# Troubleshooting AWS CloudFormation<a name="troubleshooting"></a>

When you use AWS CloudFormation, you might encounter issues when you create, update, or delete AWS CloudFormation stacks\. The following sections can help you troubleshoot some common issues that you might encounter\.

For general questions about AWS CloudFormation, see the [AWS CloudFormation FAQs](https://aws.amazon.com/cloudformation/faqs/)\. You can also search for answers and post questions in the [AWS CloudFormation forums](https://forums.aws.amazon.com/forum.jspa?forumID=92)\.

**Topics**
+ [Troubleshooting Guide](#basic-ts-guide)
+ [Troubleshooting Errors](#troubleshooting-errors)
+ [Contacting Support](#contacting-support)

## Troubleshooting Guide<a name="basic-ts-guide"></a>

If AWS CloudFormation fails to create, update, or delete your stack, you can view error messages or logs to help you learn more about the issue\. The following tasks describe general methods for troubleshooting a AWS CloudFormation issue\. For information about specific errors and solutions, see the [Troubleshooting Errors](#troubleshooting-errors) section\.
+ Use the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation/) to view the status of your stack\. In the console, you can view a list of stack events while your stack is being created, updated, or deleted\. From this list, find the failure event and then view the status reason for that event\. The status reason might contain an error message from AWS CloudFormation or from a particular service that can help you troubleshoot your problem\. For more information about viewing stack events, see [Viewing Stack Data and Resources](cfn-console-view-stack-data-resources.md)\.
+ For Amazon EC2 issues, view the cloud\-init and cfn logs\. These logs are published on the Amazon EC2 instance in the `/var/log/` directory\. These logs capture processes and command outputs while AWS CloudFormation is setting up your instance\. For Windows, view the EC2Configure service and cfn logs in `%ProgramFiles%\Amazon\EC2ConfigService` and `C:\cfn\log`\.

  You can also configure your AWS CloudFormation template so that the logs are published to Amazon CloudWatch, which displays logs in the AWS Management Console so you don't have to connect to your Amazon EC2 instance\. For more information, see [View CloudFormation Logs in the Console](https://aws.amazon.com/blogs/devops/view-cloudformation-logs-in-the-console/) in the Application Management Blog\.

## Troubleshooting Errors<a name="troubleshooting-errors"></a>

When you come across the following errors with your AWS CloudFormation stack, you can use the following solutions to help you find the source of the problems and fix them\.

**Topics**
+ [Delete Stack Fails](#troubleshooting-errors-delete-stack-fails)
+ [Dependency Error](#troubleshooting-errors-dependency-error)
+ [Error Parsing Parameter When Passing a List](#troubleshooting-errors-error-parsing-parameter-when-passing-a-list)
+ [Insufficient IAM Permissions](#troubleshooting-errors-insufficient-iam-permissions)
+ [Invalid Value or Unsupported Resource Property](#troubleshooting-errors-invalid-value-or-unsupported-resource-property)
+ [Limit Exceeded](#troubleshooting-errors-limit-exceeded)
+ [Nested Stacks are Stuck in `UPDATE_COMPLETE_CLEANUP_IN_PROGRESS`, `UPDATE_ROLLBACK_COMPLETE_CLEANUP_IN_PROGRESS`, or `UPDATE_ROLLBACK_IN_PROGRESS`](#troubleshooting-errors-nested-stacks-are-stuck)
+ [No Updates to Perform](#troubleshooting-errors-no-updates-to-perform)
+ [Resource Failed to Stabilize During a Create, Update, or Delete Stack Operation](#troubleshooting-resource-did-not-stabilize)
+ [Security Group Does Not Exist in VPC](#troubleshooting-errors-security-group-does-not-exist-in-vpc)
+ [Update Rollback Failed](#troubleshooting-errors-update-rollback-failed)
+ [Wait Condition Didn't Receive the Required Number of Signals from an Amazon EC2 Instance](#troubleshooting-errors-wait-condition-didnt-receive-the-required-number-of-signals)

### Delete Stack Fails<a name="troubleshooting-errors-delete-stack-fails"></a>

To resolve this situation, try the following:
+ Some resources must be empty before they can be deleted\. For example, you must delete all objects in an Amazon S3 bucket or remove all instances in an Amazon EC2 security group before you can delete the bucket or security group\.
+ Ensure that you have the necessary IAM permissions to delete the resources in the stack\. In addition to AWS CloudFormation permissions, you must be allowed to use the underlying services, such as Amazon S3 or Amazon EC2\.
+ When stacks are in the `DELETE_FAILED` state because AWS CloudFormation couldn't delete a resource, rerun the deletion with the [http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeleteStack.html](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeleteStack.html) parameter and specify the resource that AWS CloudFormation can't delete\. AWS CloudFormation deletes the stack without deleting the retained resource\. Retaining resources is useful when you can't delete a resource, such as an S3 bucket that contains objects that you want to keep, but you still want to delete the stack\.

  After you delete the stack, you can manually delete retained resources by using their associated AWS service\.
+ You cannot delete stacks that have termination protection enabled\. If you attempt to delete a stack with termination protection enabled, the deletion fails and the stack\-\-including its status\-\-remains unchanged\. Disable termination protection on the stack, then perform the delete operation again\. 

  This includes [nested stacks](using-cfn-nested-stacks.md) whose root stacks have termination protection enabled\. Disable termination protection on the root stack, then perform the delete operation again\. It is strongly recommended that you do not delete nested stacks directly, but only delete them as part of deleting the root stack and all its resources\.

  For more information, see [Protecting a Stack From Being Deleted](using-cfn-protect-stacks.md)\.
+ For all other issues, if you have AWS Premium Support, you can create a Technical Support case\. See [Contacting Support](#contacting-support)\.

### Dependency Error<a name="troubleshooting-errors-dependency-error"></a>

To resolve a dependency error, add a `DependsOn` attribute to resources that depend on other resources in your template\. In some cases, you must explicitly declare dependencies so that AWS CloudFormation can create or delete resources in the correct order\. For example, if you create an Elastic IP and a VPC with an Internet gateway in the same stack, the Elastic IP must depend on the Internet gateway attachment\. For additional information, see [DependsOn Attribute](aws-attribute-dependson.md)\.

### Error Parsing Parameter When Passing a List<a name="troubleshooting-errors-error-parsing-parameter-when-passing-a-list"></a>

When you use the AWS Command Line Interface or AWS CloudFormation to pass in a list, add the escape character \(`\`\) before each comma\. The following sample shows how you specify an input parameter when using the CLI\.

```
ParameterKey=CIDR,ParameterValue='10.10.0.0/16\,10.10.0.0/24\,10.10.1.0/24'
```

### Insufficient IAM Permissions<a name="troubleshooting-errors-insufficient-iam-permissions"></a>

When you work with an AWS CloudFormation stack, you not only need permissions to use AWS CloudFormation, you must also have permission to use the underlying services that are described in your template\. For example, if you're creating an Amazon S3 bucket or starting an Amazon EC2 instance, you need permissions to Amazon S3 or Amazon EC2\. Review your IAM policy and verify that you have the necessary permissions before you work with AWS CloudFormation stacks\. For more information see, [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.

### Invalid Value or Unsupported Resource Property<a name="troubleshooting-errors-invalid-value-or-unsupported-resource-property"></a>

When you create or update an AWS CloudFormation stack, your stack can fail due to invalid input parameters, unsupported resource property names, or unsupported resource property values\. For input parameters, verify that the resource exists\. For example, when you specify an Amazon EC2 key pair or VPC ID, the resource must exist in your account and in the region in which you are creating or updating your stack\. You can use AWS\-specific [parameter types](parameters-section-structure.md#parameters-section-structure-syntax) to ensure that you use valid values\.

For resource property names and values, update your template to use valid names and values\. For a list of all the resources and their property names, see [AWS Resource Types Reference](aws-template-resource-type-ref.md)\.

### Limit Exceeded<a name="troubleshooting-errors-limit-exceeded"></a>

Verify that you didn't reach a resource limit\. For example, the default number Amazon EC2 instances that you can launch is 20\. If try to create more Amazon EC2 instances than your account limit, the instance creation fails and you receive the error `Status=start_failed`\. To view the default AWS limits by service, see [AWS Service Limits](http://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) in the *AWS General Reference*\.

For AWS CloudFormation limits and tweaking strategies, see [AWS CloudFormation Limits](cloudformation-limits.md)\.

Also, during an update, if a resource is replaced, AWS CloudFormation creates new resource before it deletes the old one\. This replacement might put your account over the resource limit, which would cause your update to fail\. You can delete excess resources or request a [limit increase](http://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html)\.

### Nested Stacks are Stuck in `UPDATE_COMPLETE_CLEANUP_IN_PROGRESS`, `UPDATE_ROLLBACK_COMPLETE_CLEANUP_IN_PROGRESS`, or `UPDATE_ROLLBACK_IN_PROGRESS`<a name="troubleshooting-errors-nested-stacks-are-stuck"></a>

A nested stack failed to roll back\. Because of potential resource dependencies between nested stacks, AWS CloudFormation doesn't start cleaning up nested stack resources until all nested stacks have been updated or have rolled back\. When a nested stack fails to roll back, AWS CloudFormation cancels all operations, regardless of the state that the other nested stacks are in\. A nested stack that completed updating or rolling back but did not receive a signal from AWS CloudFormation to start cleaning up because another nested failed to roll back is in an `UPDATE_COMPLETE_CLEANUP_IN_PROGRESS` or `UPDATE_ROLLBACK_COMPLETE_CLEANUP_IN_PROGRESS` state\. A nested stack that failed to update but did not receive a signal to start rolling back is in an `UPDATE_ROLLBACK_IN_PROGRESS` state\.

A nested stack might fail to roll back because of changes that were made outside of AWS CloudFormation, when the stack template doesn't accurately reflect the state of the stack\. A nested stack might also fail if an Auto Scaling group in a nested stack had an insufficient resource signal timeout period when the group was created or updated\.

To fix the stack, contact [AWS customer support](#contacting-support)\.

### No Updates to Perform<a name="troubleshooting-errors-no-updates-to-perform"></a>

To update an AWS CloudFormation stack, you must submit template or parameter value changes to AWS CloudFormation\. However, AWS CloudFormation won't recognize some template changes as an update, such as changes to a deletion policy, update policy, condition declaration, or output declaration\. If you need to make such changes without making any other change, you can add or modify a [metadata](aws-attribute-metadata.md) attribute for any of your resources\.

For more information about modifying templates during an update, see [Modifying a Stack Template](using-cfn-updating-stacks-get-template.md)\.

### Resource Failed to Stabilize During a Create, Update, or Delete Stack Operation<a name="troubleshooting-resource-did-not-stabilize"></a>

A resource did not respond because the operation exceeded the AWS CloudFormation timeout period or an AWS service was interrupted\. For service interruptions, [check](http://status.aws.amazon.com/) that the relevant AWS service is running, and then retry the stack operation\.

If the AWS services have been running successfully, check if your stack contains one of the following resources:
+ `AWS::AutoScaling::AutoScalingGroup` for create, update, and delete operations
+ `AWS::CertificateManager::Certificate` for create operations
+ `AWS::CloudFormation::Stack` for create, update, and delete operations
+ `AWS::ElasticSearch::Domain` for update operations
+ `AWS::RDS::DBCluster` for create and update operations
+ `AWS::RDS::DBInstance` for create, update, and delete operations
+ `AWS::Redshift::Cluster` for update operations

Operations for these resources might take longer than the default timeout period\. The timeout period depends on the resource and credentials that you use\. To extend the timeout period, specify a [service role](using-iam-servicerole.md) when you perform the stack operation\. If you're already using a service role, or if your stack contains a resource that isn't listed, contact [AWS customer support](#contacting-support)\.

If your stack is in the `UPDATE_ROLLBACK_FAILED` state, see [Update Rollback Failed](#troubleshooting-errors-update-rollback-failed)\.

### Security Group Does Not Exist in VPC<a name="troubleshooting-errors-security-group-does-not-exist-in-vpc"></a>

Verify that the security group exists in the VPC that you specified\. If the security group exists, ensure that you specify the security group ID and not the security group name\. For example, the `AWS::EC2::SecurityGroupIngress` resource has a `SourceSecurityGroupName` and `SourceSecurityGroupId` properties\. For VPC security groups, you must use the `SourceSecurityGroupId` property and specify the security group ID\.

### Update Rollback Failed<a name="troubleshooting-errors-update-rollback-failed"></a>

A dependent resource cannot return to its original state, causing the rollback to fail \(`UPDATE_ROLLBACK_FAILED` state\)\. For example, you might have a stack that is rolling back to an old database instance that was deleted outside of AWS CloudFormation\. Because AWS CloudFormation doesn't know the database was deleted, it assumes that the database instance still exists and attempts to roll back to it, causing the update rollback to fail\.

Depending on the cause of the failure, you can manually fix the error and continue the rollback\. By continuing the rollback, you can return your stack to a working state \(the `UPDATE_ROLLBACK_COMPLETE` state\), and then try to update the stack again\. The following list describes solutions to common errors that cause update rollback failures:
+   
Failed to receive the required number of signals  
Use the [signal\-resource](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/signal-resource.html) command to manually send the required number of successful signals to the resource that is waiting for them, and then continue rolling back the update\. For example, during an update rollback, instances in an Auto Scaling group might fail to signal success within the specified timeout duration\. Manually send success signals to the Auto Scaling group\. When you continue the update rollback, AWS CloudFormation sees your signals and proceeds with the rollback\.
+   
Changes to a resource were made outside of AWS CloudFormation  
Manually sync resources so that they match the original stack's template, and then continue rolling back the update\. For example, if you manually deleted a resource that AWS CloudFormation is attempting to roll back to, you must manually create that resource with the same name and properties it had in the original stack\.
+   
Insufficient permissions  
Check that you have sufficient IAM permissions to modify resources, and then continue the update rollback\. For example, your IAM policy might allow you to create an S3 bucket, but not modify the bucket\. Add the modify actions to your policy\.
+   
Invalid security token  
AWS CloudFormation requires a new set of credentials\. No change is required\. Continue rolling back the update, which refreshes the credentials\.
+   
Limitation error  
Delete resources that you don't need or request a [limit increase](http://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html), and then continue rolling back the update\. For example, if your account limit for the number of EC2 instances is 20 and the update rollback exceeds that limit, it will fail\.
+   
Resource did not stabilize  
A resource did not respond because the operation might have exceeded the AWS CloudFormation timeout period or an AWS service might have been interrupted\. No change is required\. After the resource operation is complete or the AWS service is back in operation, continue rolling back the update\.

To continue rolling back an update, you can use the AWS CloudFormation console or AWS command line interface \(CLI\)\. For more information, see [Continue Rolling Back an Update](using-cfn-updating-stacks-continueupdaterollback.md)\.

If none of these solutions work, you can skip the resources that AWS CloudFormation can't successfully roll back\. For more information, see the `ResourcesToSkip` parameter for the [ContinueUpdateRollback](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ContinueUpdateRollback.html) action in the *AWS CloudFormation API Reference*\. AWS CloudFormation sets the status of the specified resources to `UPDATE_COMPLETE` and continues to roll back the stack\. After the rollback is complete, the state of the skipped resources will be inconsistent with the state of the resources in the stack template\. Before you perform another stack update, you must modify the resources or update the stack to be consistent with each other\. If you don't, subsequent stack updates might fail and make your stack unrecoverable\.

### Wait Condition Didn't Receive the Required Number of Signals from an Amazon EC2 Instance<a name="troubleshooting-errors-wait-condition-didnt-receive-the-required-number-of-signals"></a>

To resolve this situation, try the following:
+ Ensure that the AMI you're using has the AWS CloudFormation helper scripts installed\. If the AMI doesn't include the helper scripts, you can also download them to your instance\. For more information, see [CloudFormation Helper Scripts Reference](cfn-helper-scripts-reference.md)\.
+ Verify that the `cfn-signal` command was successfully run on the instance\. You can view logs, such as `/var/log/cloud-init.log` or `/var/log/cfn-init.log`, to help you debug the instance launch\. You can retrieve the logs by logging in to your instance, but you must [disable rollback on failure](cfn-console-add-tags.md) or else AWS CloudFormation deletes the instance after your stack fails to create\. You can also [publish the logs](https://aws.amazon.com/blogs/devops/view-cloudformation-logs-in-the-console/) to Amazon CloudWatch\. For Windows, you can view cfn logs in `C:\cfn\log` and EC2Config service logs in `%ProgramFiles%\Amazon\EC2ConfigService`\.
+ Verify that the instance has a connection to the Internet\. If the instance is in a VPC, the instance should be able to connect to the Internet through a NAT device if it's is in a private subnet or through an Internet gateway if it's in a public subnet\. To test the instance's Internet connection, try to access a public web page, such as `http://aws.amazon.com`\. For example, you can run the following command on the instance\. It should return an HTTP 200 status code\.

  ```
  curl -I https://aws.amazon.com
  ```

  For information about configuring a NAT device, see [NAT](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-nat.html) in the *Amazon VPC User Guide*\.

## Contacting Support<a name="contacting-support"></a>

If you have AWS Premium Support, you can create a technical support case at [https://console\.aws\.amazon\.com/support/home\#/](https://console.aws.amazon.com/support/home#/)\. Before you contact support, gather the following information:
+ The ID of the stack\. You can find the stack ID in the **Overview** tab of the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation/)\. For more information, see [Viewing Stack Data and Resources](cfn-console-view-stack-data-resources.md)\.
**Important**  
Do not make changes to the stack outside of AWS CloudFormation\. Making changes to your stack outside of AWS CloudFormation might put your stack in an unrecoverable state\.
+ Any stack error messages\. For information about viewing stack error messages, see the [Troubleshooting Guide](#basic-ts-guide) section\.
+ For Amazon EC2 issues, gather the cloud\-init and cfn logs\. These logs are published on the Amazon EC2 instance in the `/var/log/` directory\. These logs capture processes and command outputs while your instance is setting up\. For Windows, gather the EC2Configure service and cfn logs in `%ProgramFiles%\Amazon\EC2ConfigService` and `C:\cfn\log`\.

You can also search for answers and post questions in the [AWS CloudFormation forums](https://forums.aws.amazon.com/forum.jspa?forumID=92)\.