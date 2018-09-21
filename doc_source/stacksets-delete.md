# Delete Stack Sets<a name="stacksets-delete"></a>

When you are finished with the AWS CloudFormation StackSets Getting Started walkthrough, you can follow procedures in this section to delete stack sets and other resources that you have created as part of this walkthrough\. To delete a stack set, you must first delete all stack instances in the stack set\. For information about how to delete all stack instances, see [Delete Stack Instances](stackinstances-delete.md)\.

## Delete Stack Set<a name="stacksets-delete-set"></a>

After you have deleted all stack instances, you can delete the stack set\.

**To delete a stack set by using the AWS Management Console**

1. On the StackSets home page, select the stack set that you created in [Create a New Stack Set](stacksets-getting-started-create.md)\. In this walkthrough, we created a stack set named `my-awsconfig-stackset`\.  
![\[Select stack set\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_my_awsconfig.png)

1. With the stack set selected, choose **Delete stack set** from the **Actions** menu\.

1. When you are prompted to confirm that you want to delete the stack set, choose **Yes, Delete**\.  
![\[Delete stack set confirmation\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stacksets_delete_stackset.png)

**To delete a stack set by using the AWS CLI**

1. Run the following command\. When you are prompted to confirm, type **y**, and then press **Enter**\.

   ```
   aws cloudformation delete-stack-set --stack-set-name my-awsconfig-stackset
   ```

1. Verify that the stack set was deleted by running the `list-stack-sets` command\. The results of the list\-stack\-sets command should show your stack with a status of `DELETED`\.

   ```
   aws cloudformation list-stack-sets
   ```

## Delete Service Roles \(Optional\)<a name="stacksets-delete-roles"></a>

Delete the service roles that you created as part of the [Prerequisites: Granting Permissions for Stack Set Operations](stacksets-prereqs.md) for the walkthrough in this guide\. The roles that you created to get started with StackSets are named **AWSCloudFormationStackSetAdministrationRole** in the administrator account, and **AwsCloudFormationStackSetExecutionRole** in each target account\. For more information about deleting roles, see [Deleting Roles and Instance Profiles](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_manage_delete.html) in the *IAM User Guide*\.

**To delete a service role by using the AWS Management Console**

1. Sign in to the AWS Management Console and open the IAM console at [https://console\.aws\.amazon\.com/iam/](https://console.aws.amazon.com/iam/)\.

1. In the navigation pane, choose **Roles**, and then fill the check box next to the role that you want to delete\.

1. In the **Role actions** menu at the top of the page, choose **Delete role**\.

1. In the confirmation dialog box, choose **Yes, Delete**\. If you are sure, you can proceed with the deletion even if the service last accessed data is still loading\.

**To delete a service role by using the AWS CLI**
+ Run the following command\. When you are prompted to confirm, type **y**, and then press **Enter**\.

  ```
  aws iam delete-role --role-name role name
  ```