# Deleting a stack on the AWS CloudFormation console<a name="cfn-console-delete-stack"></a>

**To delete a stack**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. On the **Stacks** page in the CloudFormation console, select the stack that you want to delete\. The stack must be currently running\.

1. In the stack details pane, choose **Delete**\.

1. Select **Delete stack** when prompted\.
**Note**  
After stack deletion has begun, you cannot abort it\. The stack proceeds to the **DELETE\_IN\_PROGRESS** state\.

   After the stack deletion is complete, the stack will be in the **DELETE\_COMPLETE** state\. Stacks in the **DELETE\_COMPLETE** state are not displayed in the AWS CloudFormation console by default\. To display deleted stacks, you must change the stack view filter as described in [Viewing deleted stacks on the AWS CloudFormation consoleViewing deleted stacks](cfn-console-view-deleted-stacks.md)\.

   If the delete failed, the stack will be in the **DELETE\_FAILED** state\. For solutions, see the [Delete stack fails](troubleshooting.md#troubleshooting-errors-delete-stack-fails) troubleshooting topic\.

For information on protecting stacks from being accidentally deleted see [Protecting a stack from being deleted](using-cfn-protect-stacks.md)\.