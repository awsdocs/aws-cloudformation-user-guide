# Updating stacks using change sets<a name="using-cfn-updating-stacks-changesets"></a>

When you need to update a stack, understanding how your changes will affect running resources before you implement them can help you update stacks with confidence\. Change sets allow you to preview how proposed changes to a stack might impact your running resources, for example, whether your changes will delete or replace any critical resources, AWS CloudFormation makes the changes to your stack only when you decide to execute the change set, allowing you to decide whether to proceed with your proposed changes or explore other changes by creating another change set\. You can create and manage change sets using the AWS CloudFormation console, AWS CLI, or AWS CloudFormation API\.

**Topics**
+ [Creating a change set](using-cfn-updating-stacks-changesets-create.md)
+ [Viewing a change set](using-cfn-updating-stacks-changesets-view.md)
+ [Executing a change set](using-cfn-updating-stacks-changesets-execute.md)
+ [Deleting a change set](using-cfn-updating-stacks-changesets-delete.md)
+ [Example change sets](using-cfn-updating-stacks-changesets-samples.md)

**Important**  
Change sets don't indicate whether AWS CloudFormation will successfully update a stack\. For example, a change set doesn't check if you will surpass an account [limit](cloudformation-limits.md), if you're updating a [resource](aws-template-resource-type-ref.md) that doesn't support updates, or if you have insufficient [permissions](using-iam-template.md) to modify a resource, all of which can cause a stack update to fail\. If an update fails, AWS CloudFormation attempts to roll back your resources to their original state\.

Change Set Overview

The following diagram summarizes how you use change sets to update a stack:

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/update-stack-changesets-diagram.png)

1. Create a change set by submitting changes for the stack that you want to update\. You can submit a modified stack template or modified input parameter values\. AWS CloudFormation compares your stack with the changes that you submitted to generate the change set; it doesn't make changes to your stack at this point\.

1. View the change set to see which stack settings and resources will change\. For example, you can see which resources AWS CloudFormation will add, modify, or delete\.

1. Optional: If you want to consider other changes before you decide which changes to make, create additional change sets\. Creating multiple change sets helps you understand and evaluate how different changes will affect your resources\. You can create as many change sets as you need\.

1. Execute the change set that contains the changes that you want to apply to your stack\. AWS CloudFormation updates your stack with those changes\.
**Note**  
After you execute a change, AWS CloudFormation removes all change sets that are associated with the stack because they aren't applicable to the updated stack\.

You can also delete change sets to prevent executing a change set that shouldn't be applied\.