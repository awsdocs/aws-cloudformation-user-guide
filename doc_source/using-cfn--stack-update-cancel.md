# Canceling a stack update<a name="using-cfn--stack-update-cancel"></a>

After a stack update has begun, you can cancel the stack update if the stack is still in the `UPDATE_IN_PROGRESS` state\. After an update has finished, you cannot cancel it\. You can, however, update a stack again with any previous settings\.

If you cancel a stack update, the stack is rolled back to the stack configuration that existed prior to initiating the stack update\.

**Topics**
+ [To cancel a stack update by using the console](#using-cfn--stack-update-cancel-console)
+ [To cancel a stack update by using the command line](#using-cfn--stack-update-cancel-cli)

## To cancel a stack update by using the console<a name="using-cfn--stack-update-cancel-console"></a>

1. From the list of stacks in the AWS CloudFormation console, select the stack that is currently being updated\. Its status must be **UPDATE\_IN\_PROGRESS**\.

1. Choose **Stack actions** and then **Cancel update stack**\.

1. To continue canceling the update, click **Cancel update**\. Otherwise, click **Cancel** to resume the update\.

The stack proceeds to the **UPDATE\_ROLLBACK\_IN\_PROGRESS** state\. After the update cancellation is complete, the stack is set to **UPDATE\_ROLLBACK\_COMPLETE**\.

## To cancel a stack update by using the command line<a name="using-cfn--stack-update-cancel-cli"></a>
+ Use the command [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/cancel-update-stack.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/cancel-update-stack.html) to cancel an update\.