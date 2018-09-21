# Deleting a Stack on the AWS CloudFormation Console<a name="cfn-console-delete-stack"></a>

**To delete a stack**

1. From the list of stacks in the AWS CloudFormation console, select the stack that you want to delete \(it must be currently running\)\.

1. Choose **Actions** and then **Delete Stack**\.  
![\[The Delete Stack option in the Actions menu.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cfn-console-delete-stack.png)

1. Click **Yes, Delete** when prompted\.
**Note**  
After stack deletion has begun, you cannot abort it\. The stack proceeds to the **DELETE\_IN\_PROGRESS** state\.

   After the stack deletion is complete, the stack will be in the **DELETE\_COMPLETE** state\. Stacks in the **DELETE\_COMPLETE** state are not displayed in the AWS CloudFormation console by default\. To display deleted stacks, you must change the stack view setting as described in [Viewing Deleted Stacks](cfn-console-view-deleted-stacks.md)\.

   If the delete failed, the stack will be in the **DELETE\_FAILED** state\. For solutions, see the [Delete Stack Fails](troubleshooting.md#troubleshooting-errors-delete-stack-fails) troubleshooting topic\.

For information on protecting stacks from being accidently deleted see [Protecting a Stack From Being Deleted](using-cfn-protect-stacks.md)\.