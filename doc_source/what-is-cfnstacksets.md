# Working with AWS CloudFormation StackSets<a name="what-is-cfnstacksets"></a>

AWS CloudFormation StackSets extends the functionality of stacks by enabling you to create, update, or delete stacks across multiple accounts and regions with a single operation\. Using an administrator account, you define and manage an AWS CloudFormation template, and use the template as the basis for provisioning stacks into selected target accounts across specified regions\.

![\[A stack set is a collection of resources, defined in a template and deployed into one or more accounts across one or more regions.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stack_set_conceptual_sv.png)

This section helps you get started using StackSets, and answers common questions about how to work with and troubleshoot stack set creation, updates, and deletion\.

**Topics**
+ [StackSets Concepts](stacksets-concepts.md)
+ [Prerequisites: Granting Permissions for Stack Set Operations](stacksets-prereqs.md)
+ [Getting Started with AWS CloudFormation StackSets](stacksets-getting-started.md)
+ [Configuring a target account gate in AWS CloudFormation StackSets](stacksets-account-gating.md)
+ [Best Practices](stacksets-bestpractices.md)
+ [Limitations of StackSets](stacksets-limitations.md)
+ [AWS CloudFormation StackSets Sample Templates](stacksets-sampletemplates.md)
+ [Troubleshooting AWS CloudFormation StackSets](stacksets-troubleshooting.md)