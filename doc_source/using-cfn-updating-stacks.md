# AWS CloudFormation stack updates<a name="using-cfn-updating-stacks"></a>

When you need to make changes to a stack's settings or change its resources, you update the stack instead of deleting it and creating a new stack\. For example, if you have a stack with an EC2 instance, you can update the stack to change the instance's AMI ID\.

When you update a stack, you submit changes, such as new input parameter values or an updated template\. AWS CloudFormation compares the changes you submit with the current state of your stack and updates only the changed resources\. For a summary of the update workflow, see [How does AWS CloudFormation work?](cfn-whatis-howdoesitwork.md)\.

**Note**  
When updating a stack, AWS CloudFormation might interrupt resources or replace updated resources, depending on which properties you update\. For more information about resource update behaviors, see [Update behaviors of stack resources](using-cfn-updating-stacks-update-behaviors.md)\.

 **Update methods** 

AWS CloudFormation provides two methods for updating stacks: *direct update* or creating and executing *change sets*\. When you directly update a stack, you submit changes and AWS CloudFormation immediately deploys them\. Use direct updates when you want to quickly deploy your updates\.

With change sets, you can preview the changes AWS CloudFormation will make to your stack, and then decide whether to apply those changes\. Change sets are JSON\-formatted documents that summarize the changes AWS CloudFormation will make to a stack\. Use change sets when you want to ensure that AWS CloudFormation doesn't make unintentional changes or when you want to consider several options\. For example, you can use a change set to verify that AWS CloudFormation won't replace your stack's database instances during an update\.

**Topics**
+ [Update behaviors of stack resources](using-cfn-updating-stacks-update-behaviors.md)
+ [Modifying a stack template](using-cfn-updating-stacks-get-template.md)
+ [Updating stacks using change sets](using-cfn-updating-stacks-changesets.md)
+ [Updating stacks directly](using-cfn-updating-stacks-direct.md)
+ [Monitoring the progress of a stack update](using-cfn-updating-stacks-monitor-stack.md)
+ [Canceling a stack update](using-cfn--stack-update-cancel.md)
+ [Prevent updates to stack resources](protect-stack-resources.md)
+ [Continue rolling back an update](using-cfn-updating-stacks-continueupdaterollback.md)