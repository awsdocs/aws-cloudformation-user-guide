# Creating stacks using change sets<a name="cfn-console-create-stacks-changesets"></a>

To preview how a AWS CloudFormation stack will be configured before creating the stack, create a change set\. This functionality allows you to examine various configurations and make corrections and changes to your stack before executing the change set\. For more information on change sets, see [Updating stacks using change sets](using-cfn-updating-stacks-changesets.md)\.

## Creating a change set for a new stack<a name="cfn-console-create-stacks-changesets-create-new-stack"></a>

To create a change set for a new stack, select your stack template and specify the configuration of your stack as you would if you were creating a new stack, then choose to create a new change set rather than a new stack\.

**To create a change set using the CloudFormation console**

1. [Start the Create stack wizard](cfn-console-create-stack.md)

1. [Select a stack template](cfn-using-console-create-stack-template.md)

1. [Specify parameters for your stack](cfn-using-console-create-stack-parameters.md)

1. [Set stack options](cfn-console-add-tags.md)

1. On the **Review** page, review the details of your stack\.

   If you need to change any of the settings before you create the change set, click **Edit** on the appropriate section to go back to the page that has the setting that you want to change\.

1. Click **Create change set**\.

1. Enter a name for the change set, and a description if desired\. Click **Create change set**\.

   When you create a change set for a new stack, CloudFormation does the following:
   + Launches a new stack with a status of **REVIEW\_IN\_PROGRESS**\. 
   + Creates a change set for the new stack that reflects the stack configuration you specified in the steps above\. 

   CloudFormation displays the **Change sets** page for the proposed stack\. While AWS CloudFormation creates the change set, its status is **CREATE\_IN\_PROGRESS**, and its execution status is **UNAVAILABLE**\. When AWS CloudFormation completes succesfully creating the change set, it sets the change set status to **CREATE\_COMPLETE**, and its execution status is **AVAILABLE**\. The stack status is updated to **REVIEW\_IN\_PROGRESS**\. At this point, you can execute the change set to complete creating the new stack\.

   In the **Changes** pane, AWS CloudFormation displays the proposed configuration of your stack\.

   If AWS CloudFormation fails to create the change set, it sets the changes set status to **CREATE\_FAILED**\. Fix the error displayed in the **Status reason** field, and then create a new change set\. At this stage, you can try various configurations and make corrections and changes to your stack before executing the next change set\.

1. To complete creating a new stack based on the change set, choose **Execute**, and then choose **Execute** again\.