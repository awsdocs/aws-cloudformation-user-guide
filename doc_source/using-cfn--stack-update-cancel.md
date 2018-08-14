# Canceling a Stack Update<a name="using-cfn--stack-update-cancel"></a>

After a stack update has begun, you can cancel the stack update if the stack is still in the `UPDATE_IN_PROGRESS` state\. After an update has finished, you cannot cancel it\. You can, however, update a stack again with any previous settings\.

If you cancel a stack update, the stack is rolled back to the stack configuration that existed prior to initiating the stack update\.

**Topics**
+ [To cancel a stack update by using the console](#w3ab2c15c17c27b9)
+ [To cancel a stack update by using the command line](#w3ab2c15c17c27c11)

## To cancel a stack update by using the console<a name="w3ab2c15c17c27b9"></a>

1. From the list of stacks in the AWS CloudFormation console, select the stack that is currently being updated \(its state must be `UPDATE_IN_PROGRESS`\) \.

1. Choose **Actions** and then **Cancel Update**\.  
![\[The Cancel Update option in the Actions menu.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cfn-cancel-stack-update.png)

1. To continue canceling the update, click **Yes, Cancel Update** when prompted\. Otherwise, click **Cancel** to resume the update\.

The stack proceeds to the **UPDATE\_ROLLBACK\_IN\_PROGRESS** state\. After the update cancellation is complete, the stack is set to **UPDATE\_ROLLBACK\_COMPLETE**\.

## To cancel a stack update by using the command line<a name="w3ab2c15c17c27c11"></a>
+ Use the command [http://docs.aws.amazon.com/cli/latest/reference/cloudformation/cancel-update-stack.html](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/cancel-update-stack.html) to cancel an update\.