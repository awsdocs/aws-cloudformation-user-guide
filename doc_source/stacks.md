# Working with stacks<a name="stacks"></a>

A stack is a collection of AWS resources that you can manage as a single unit\. In other words, you can create, update, or delete a collection of resources by creating, updating, or deleting stacks\. All the resources in a stack are defined by the stack's AWS CloudFormation template\. A stack, for instance, can include all the resources required to run a web application, such as a web server, a database, and networking rules\. If you no longer require that web application, you can simply delete the stack, and all of its related resources are deleted\.

AWS CloudFormation ensures all stack resources are created or deleted as appropriate\. Because AWS CloudFormation treats the stack resources as a single unit, they must all be created or deleted successfully for the stack to be created or deleted\. If a resource cannot be created, AWS CloudFormation rolls the stack back and automatically deletes any resources that were created\. If a resource cannot be deleted, any remaining resources are retained until the stack can be successfully deleted\.

You can work with stacks by using the AWS CloudFormation [console](https://console.aws.amazon.com/cloudformation/), [API](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/), or [AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/cloudformation)\.

**Note**  
You are charged for the stack resources for the time they were operating \(even if you deleted the stack right away\)\.

**Topics**
+ [Using the AWS CloudFormation console](cfn-using-console.md)
+ [Using the AWS Command Line Interface](cfn-using-cli.md)
+ [AWS CloudFormation stack updates](using-cfn-updating-stacks.md)
+ [Detecting unmanaged configuration changes to stacks and resources](using-cfn-stack-drift.md)
+ [Bringing existing resources into CloudFormation management](resource-import.md)
+ [Moving resources between stacks](refactor-stacks.md)
+ [Resources that support import and drift detection operations](resource-import-supported-resources.md)
+ [Exporting stack output values](using-cfn-stack-exports.md)
+ [Listing stacks that import an exported output value](using-cfn-stack-imports.md)
+ [Working with nested stacks](using-cfn-nested-stacks.md)
+ [Working with Microsoft Windows stacks on AWS CloudFormation](cfn-windows-stacks.md)