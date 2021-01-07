# Executing a change set<a name="using-cfn-updating-stacks-changesets-execute"></a>

To make the changes described in a change set to your stack, execute the change set\.

**Important**  
After you execute a change set, AWS CloudFormation deletes any additional change sets that are associated with the stack because they are no longer valid for the updated stack\. If an update fails, you need to create a new change set\.

**Stack Policies and Executing a Change Set**  
If you execute a change set on a stack that has a stack policy associated with it, AWS CloudFormation enforces the policy when it updates the stack\. You can't specify a temporary stack policy that overrides the existing policy when you execute a change set\. To update a protected resource, you must update the stack policy or use the [direct update](using-cfn-updating-stacks-direct.md) method\.

------
#### [ Execute a change set for nested stacks \(console\) ]

**To execute a change set for nested stacks \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), in **Stacks**, choose the name the stack that you want to update\. You must choose the stack name associated with the root change set\.

1. In the navigation pane, choose **Change Sets** to view a list of the stack's change sets\.

1. Choose the name of the root change set that you want to execute\.

1. On the change set's details page, choose **Execute**\.
**Note**  
AWS CloudFormation executes the changes described in your root change set and nested change sets, if **Enabled** for change sets for nested stacks was selected during the [Creating a change set](using-cfn-updating-stacks-changesets-create.md) process\.   
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-change-sets-delete-and-execute.png)

   AWS CloudFormation immediately starts updating the stack\. The AWS CloudFormation console directs you to the [**Events**](cfn-console-view-stack-data-resources.md) tab, where you can monitor the progress of the stack update\.

------
#### [ Execute a change set \(console\) ]

**To execute a change set \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), in **Stacks**, choose the name the stack that you want to update\.

1. In the navigation pane, choose **Change Sets** to view a list of the stack's change sets\.

1. Choose the name of the change set that you want to execute\.

1. On the change set's details page, choose **Execute**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-change-sets-delete-and-execute.png)

   AWS CloudFormation immediately starts updating the stack\. The AWS CloudFormation console directs you to the [**Events**](cfn-console-view-stack-data-resources.md) tab, where you can monitor the progress of the stack update\.

------

**To execute a change set \(AWS CLI\)**
+ Run the [aws cloudformation execute\-change\-set](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/execute-change-set.html) command\.

  Specify the change set ID of the change set that you want to execute, as shown in the following example:

  ```
  aws cloudformation execute-change-set --change-set-name arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000
  ```

  The command in the example executes a change set with the ID `arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000`\.

  After you run the command, AWS CloudFormation starts updating the stack\. To view the stack's progress, use the [aws cloudformation describe\-stacks](using-cfn-describing-stacks.md) command\.