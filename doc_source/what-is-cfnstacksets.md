# Working with AWS CloudFormation StackSets<a name="what-is-cfnstacksets"></a>

AWS CloudFormation StackSets extends the capability of stacks by enabling you to create, update, or delete stacks across multiple accounts and AWS Regions with a single operation\. Using an administrator account, you define and manage an AWS CloudFormation template, and use the template as the basis for provisioning stacks into selected target accounts across specified AWS Regions\.

![\[A stack set is a collection of resources, defined in a template and deployed into one or more accounts across one or more regions.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stack_set_conceptual_sv.png)

For information about StackSets region support see, [StackSets regional support](https://docs.aws.amazon.com/general/latest/gr/cfn.html#regional-support-stacksets)\.

This section helps you get started using StackSets, and answers common questions about how to work with and troubleshoot stack set creation, updates, and deletion\.

**Topics**
+ [StackSets concepts](stacksets-concepts.md)
+ [Prerequisites for stack set operations](stacksets-prereqs.md)
+ [Getting started with AWS CloudFormation StackSets](stacksets-getting-started.md)
+ [Configuring a target account gate in AWS CloudFormation StackSets](stacksets-account-gating.md)
+ [Detecting unmanaged configuration changes in stack sets](stacksets-drift.md)
+ [Importing a stack into AWS CloudFormation StackSets](stacksets-import.md)
+ [Account level targets for service\-managed Stack Sets](account-level-targets.md)
+ [Best practices](stacksets-bestpractices.md)
+ [AWS CloudFormation StackSets sample templates](stacksets-sampletemplates.md)
+ [Troubleshooting AWS CloudFormation StackSets](stacksets-troubleshooting.md)