# Executing a Change Set<a name="using-cfn-updating-stacks-changesets-execute"></a>

To make the changes described in a change set to your stack, execute the change set\.

**Important**  
After you execute a change set, AWS CloudFormation deletes all change sets that are associated with the stack because they aren't valid for the updated stack\. If an update fails, you need to create a new change set\.

Stack Policies and Executing a Change Set

If you execute a change set on a stack that has a stack policy associated with it, AWS CloudFormation enforces the policy when it updates the stack\. You can't specify a temporary stack policy that overrides the existing policy when you execute a change set\. To update a protected resource, you must update the stack policy or use the [direct update](using-cfn-updating-stacks-direct.md) method\.

**To execute a change set \(console\)**

1. In the AWS CloudFormation console, choose the stack that you want to update\.

1. In the stack detail pane, choose **Change Sets** to view a list of the stack's change sets\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-changeset-tab.png)

1. Choose the change set that you want execute\.

   The AWS CloudFormation console directs you to the detail page of the change set\.

1. Choose **Execute**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-changeset-execute.png)

1. Confirm that this is the change set you want to execute, and then choose **Execute**\.

   AWS CloudFormation immediately starts updating the stack\. You can monitor the progress of the update by viewing the [**Events**](cfn-console-view-stack-data-resources.md) tab\.

**To execute a change set \(AWS CLI\)**
+ Run the [aws cloudformation execute\-change\-set](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/execute-change-set.html) command\.

  Specify the change set ID of the change set that you want to execute, as shown in the following example:

  ```
  aws cloudformation execute-change-set --change-set-name arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000
  ```

  The command in the example executes a change set with the ID `arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000`\.

  After you run the command, AWS CloudFormation starts updating the stack\. To view the stack's progress, use the [aws cloudformation describe\-stacks](using-cfn-describing-stacks.md) command\.