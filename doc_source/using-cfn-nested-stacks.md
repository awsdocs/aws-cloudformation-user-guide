# Working with nested stacks<a name="using-cfn-nested-stacks"></a>

*Nested stacks* are stacks created as part of other stacks\. You create a nested stack within another stack by using the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html) resource\.

As your infrastructure grows, common patterns can emerge in which you declare the same components in multiple templates\. You can separate out these common components and create dedicated templates for them\. Then use the resource in your template to reference other templates, creating nested stacks\.

For example, assume that you have a load balancer configuration that you use for most of your stacks\. Instead of copying and pasting the same configurations into your templates, you can create a dedicated template for the load balancer\. Then, you just use the resource to reference that template from within other templates\.

Nested stacks can themselves contain other nested stacks, resulting in a hierarchy of stacks, as in the diagram below\. The *root stack* is the top\-level stack to which all the nested stacks ultimately belong\. In addition, each nested stack has an immediate *parent stack*\. For the first level of nested stacks, the root stack is also the parent stack\. in the diagram below, for example:
+ Stack A is the root stack for all the other, nested, stacks in the hierarchy\.
+ For stack B, stack A is both the parent stack, as well as the root stack\.
+ For stack D, stack C is the parent stack; while for stack C, stack B is the parent stack\.

![\[Nested stacks, which are created as part of another stack, have an immediate parent stack, as well as the top-level root stack.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cfn-console-nested-stacks.png)

Using nested stacks to declare common components is considered a [best practice](best-practices.md#nested)\. 

Certain stack operations, such as stack updates, should be initiated from the root stack rather than performed directly on nested stacks themselves\. Also, in some cases, nested stacks affect how stack operations are performed\. For more information, refer to the following topics: 
+ [Use nested stacks to reuse common template patterns](best-practices.md#nested)
+ [Protecting a stack from being deleted](using-cfn-protect-stacks.md)
+ [Update behaviors of stack resources](using-cfn-updating-stacks-update-behaviors.md)
+ [Exporting stack output values vs\. using nested stacks](using-cfn-stack-exports.md#output-vs-nested)
+ [Using `ResourcesToSkip` to recover a nested stacks hierarchy](using-cfn-updating-stacks-continueupdaterollback.md#nested-stacks)
+ [Nested stacks are stuck in `UPDATE_COMPLETE_CLEANUP_IN_PROGRESS`, `UPDATE_ROLLBACK_COMPLETE_CLEANUP_IN_PROGRESS`, or `UPDATE_ROLLBACK_IN_PROGRESS`](troubleshooting.md#troubleshooting-errors-nested-stacks-are-stuck)

**To view the root stack of a nested stack**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\. Select the stack that you want\.

   Nested stacks display **NESTED** next to their stack name\.

1. On the **Overview** tab, click the stack name listed as **Root stack**\.

**To view the nested stacks that belong to a root stack**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\. Click the name of the root stack whose nested stacks you want to view\.

1. Expand the **Resources** section\.

   Look for resources of type **AWS::CloudFormation::Stack**\.

**Topics**
+ [Change sets for nested stacks](change-sets-for-nested-stacks.md)
+ [Nesting an existing stack](resource-import-nested-stacks.md)