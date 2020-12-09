# Deleting a change set<a name="using-cfn-updating-stacks-changesets-delete"></a>

Deleting a change set removes it from the list of change sets for the stack\. Deleting a change set prevents you or another user from accidentally executing a change set that shouldn't be applied\. Unless you delete them, AWS CloudFormation retains all change sets until you update the stack\.

------
#### [ Delete a change set for nested stacks ]

**To delete a change set for nested stacks \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), in **Stacks**, select the stack name associated with the root change set\.

1. In the navigation pane, choose **Change Sets** to view a list of the stack's change sets\.

1. Select the name of the change set that you want to delete\. 

1. On the change set's details page, choose **Delete**\. By choosing **Delete**, you will delete the whole hierarchy of nested change sets\.
**Note**  
The delete operation for change sets for nested stacks is asynchronous and will show a `DELETE_PENDING` status, followed by a `DELETE_IN_PROGRESS` status\. Upon completion of the delete change set operation, the change sets will be removed from the list\. Nested stacks in the `REVIEW_IN_PROGRESS` status will also be deleted if they were created during the change set creation\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-change-sets-delete-and-execute.png)

   AWS CloudFormation immediately starts to delete the change set from the stack's list of change sets\.
**Note**  
If you have nested stacks that are stuck in an in\-progress operation, see Troubleshooting Errors in [Troubleshooting AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/troubleshooting.html#troubleshooting-errors-nested-stacks-are-stuck)\.

------
#### [ Delete a change set ]

**To delete a change set \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), in **Stacks**, select the name of the stack that contains the change set that you want to delete\.

1. In the navigation pane, choose **Change Sets** to view a list of the stack's change sets\.

1. Select the name of the change set that you want to delete\.

1. On the change set's details page, choose **Delete**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-change-sets-delete-and-execute.png)

   AWS CloudFormation immediately starts to delete the change set from the stack's list of change sets, and you're redirected to the **Stacks** page\. 

------

**To delete a change set \(AWS CLI\)**
+ Run the [aws cloudformation delete\-change\-set](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/delete-change-set.html) command, specifying the ID of the change set that you want to delete, as shown in the following example:

  ```
  aws cloudformation delete-change-set --change-set-name arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000
  ```