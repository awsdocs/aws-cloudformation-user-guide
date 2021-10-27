# Deleting a stack on the AWS CloudFormation console<a name="cfn-console-delete-stack"></a>

**To delete a stack**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. On the **Stacks** page in the CloudFormation console, select the stack that you want to delete\. The stack must be currently running\.

1. In the stack details pane, choose **Delete**\.

1. Select **Delete stack** when prompted\.
**Note**  
The stack deletion operation can't be stopped once the stack deletion has begun\. The stack proceeds to the `DELETE_IN_PROGRESS` state\.

   After the stack deletion is complete, the stack will be in the `DELETE_COMPLETE` state\. Stacks in the `DELETE_COMPLETE` state aren't displayed in the CloudFormation console by default\. To display deleted stacks, you must change the stack view filter as described in [Viewing deleted stacks on the AWS CloudFormation consoleViewing deleted stacks](cfn-console-view-deleted-stacks.md)\.

   If the delete failed, the stack will be in the `DELETE_FAILED` state\. For solutions, see the [Delete stack fails](troubleshooting.md#troubleshooting-errors-delete-stack-fails)troubleshooting topic\.

For information on protecting stacks from being accidentally deleted see [Protecting a stack from being deleted](using-cfn-protect-stacks.md)\.