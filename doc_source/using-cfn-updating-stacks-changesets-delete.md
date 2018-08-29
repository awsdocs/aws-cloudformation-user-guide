# Deleting a Change Set<a name="using-cfn-updating-stacks-changesets-delete"></a>

Deleting a change set removes it from the list of change sets for the stack\. Deleting a change set prevents you or another user from accidentally executing a change set that shouldn't be applied\. AWS CloudFormation retains all change sets until you update the stack unless you delete them\.

**To delete a change set \(console\)**

1. In the AWS CloudFormation console, choose the stack that contains the change set that you want to delete\.

1. In the stack detail pane, choose **Change Sets** to view a list of the stack's change sets\.

1. Choose the change set that you want delete\.

   The AWS CloudFormation console directs you to the detail page for the change set\.

1. Choose **Other Actions**, and then choose **Delete**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-changeset-delete.png)

1. Confirm that this is the change set you want to delete, and then choose **Delete**\.

   AWS CloudFormation deletes the change set from the stack's list of change sets\.

**To delete a change set \(AWS CLI\)**
+ Run the [aws cloudformation delete\-change\-set](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/delete-change-set.html) command, specifying the ID of the change set that you want to delete, as shown in the following example:

  ```
  aws cloudformation delete-change-set --change-set-name arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000
  ```