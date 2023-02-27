# Importing a stack into AWS CloudFormation StackSets<a name="stacksets-import"></a>

The AWS CloudFormation *stack import* operation can import existing stacks into new or existing stack sets, so that you can migrate existing stacks to a stack set in one operation\. *StackSets* extends the functionality of stacks, so you can create, update, or delete stacks across multiple accounts and Regions with a single operation\.

Use the stack import operations for *self\-managed* or *service\-managed* StackSets\. For *self\-managed* StackSets, the import operation can import stacks in the administrator account or in different target accounts and AWS Regions\. For *service\-managed* StackSets, the import operation can import any stack in the same AWS Organizations as the management account\. The import operation can import up to 10 stacks using inline stack IDs or up to 200 stacks using an Amazon S3 object\.

Stack import is available wherever StackSets are supported\. For information about StackSets Region support, see [StackSets regional support](https://docs.aws.amazon.com/general/latest/gr/cfn.html#regional-support-stacksets)\.

## Requirements for stack import<a name="stackset-import-considerations"></a>

Because stack sets perform stack operations across multiple accounts, before you can create your first stack set you need the necessary permissions defined in your AWS account\.
+ To set up the required permissions for creating a stack set with **self\-managed** permissions, see [Performing stack set operations involving regions that are disabled by default](stacksets-prereqs.md#stacksets-opt-in-regions) and [Grant self\-managed permissions](stacksets-prereqs-self-managed.md)\.
+ To set up the required permissions for creating a stack set with **service\-managed** permissions, see [Performing stack set operations involving regions that are disabled by default](stacksets-prereqs.md#stacksets-opt-in-regions) and [Enable trusted access with AWS Organizations](stacksets-orgs-enable-trusted-access.md)\.

For more information on StackSets requirements, see [Prerequisites for stack set operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs.html)\.

Before you import a stack into a stack set, make sure you understand the following requirements:
+ Stacks can only belong to one stack set\.
+ You can implement stack tags to the stack set by specifying tags explicitly as parameters in the stack import operation\.
+ A stack's custom parameter overrides aren't affected during the import operation\.
+ The StackSets quotas and stack instances apply when importing stacks\. For more information about quotas, see [AWS CloudFormation quotas](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html)\.

**Topics**
+ [Requirements for stack import](#stackset-import-considerations)
+ [Self\-managed stack import for AWS CloudFormation StackSets](self-managed-import.md)
+ [Service\-managed stack import for AWS CloudFormation StackSets](service-managed-import.md)
+ [Reverting a stack import operation](reverting-stackset-import.md)