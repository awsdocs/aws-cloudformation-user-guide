# Working with AWS CloudFormation StackSets<a name="what-is-cfnstacksets"></a>

AWS CloudFormation StackSets extends the functionality of stacks by enabling you to create, update, or delete stacks across multiple accounts and regions with a single operation\. Using an administrator account, you define and manage an AWS CloudFormation template, and use the template as the basis for provisioning stacks into selected target accounts across specified regions\.

![\[A stack set is a collection of resources, defined in a template and deployed into one or more accounts across one or more regions.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stack_set_conceptual_sv.png)

For information about StackSets region support see, [StackSets regional support](https://docs.aws.amazon.com/general/latest/gr/cfn.html#regional-support-stacksets)\.

This section helps you get started using StackSets, and answers common questions about how to work with and troubleshoot stack set creation, updates, and deletion\.

**Topics**
+ [StackSets concepts](stacksets-concepts.md)
+ [Prerequisites for stack set operations](stacksets-prereqs.md)
+ [Getting started with AWS CloudFormation StackSets](stacksets-getting-started.md)
+ [Configuring a target account gate in AWS CloudFormation StackSets](stacksets-account-gating.md)
+ [Detecting unmanaged configuration changes in stack sets](stacksets-drift.md)
+ [Best practices](stacksets-bestpractices.md)
+ [AWS CloudFormation StackSets sample templates](stacksets-sampletemplates.md)
+ [Troubleshooting AWS CloudFormation StackSets](stacksets-troubleshooting.md)