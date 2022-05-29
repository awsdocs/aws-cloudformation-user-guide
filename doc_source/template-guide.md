# Working with AWS CloudFormation templates<a name="template-guide"></a>

To provision and configure your stack resources, you must understand AWS CloudFormation templates, which are formatted text files in JSON or YAML\. These templates describe the resources that you want to provision in your AWS CloudFormation stacks\. You can use AWS CloudFormation Designer or any text editor to create and save templates\. For information about the structure and syntax of a template, see [Template anatomy](template-anatomy.md)\.

If you're unfamiliar with JSON or YAML, you can use AWS CloudFormation Designer to help you get started with AWS CloudFormation templates\. AWS CloudFormation Designer is a tool for visually creating and modifying templates\. For more information, see [What is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)\.

[Template snippets](CHAP_TemplateQuickRef.md) provides examples that demonstrate how to write templates for a particular resource\. For example, you can view snippets for Amazon EC2 instances, Amazon S3 domains, AWS CloudFormation mappings, and more\. Snippets are grouped by resource, with general\-purpose AWS CloudFormation snippets in [General template snippets](quickref-general.md)\.

For details about the supported resources, type names, intrinsic functions, and pseudo parameters you can use in your templates, see [Template reference](template-reference.md)\.

**Topics**
+ [AWS CloudFormation template formats](template-formats.md)
+ [Template anatomy](template-anatomy.md)
+ [What is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)
+ [Walkthroughs](CHAP_Using.md)
+ [Template snippets](CHAP_TemplateQuickRef.md)
+ [Custom resources](template-custom-resources.md)
+ [Using AWS CloudFormation macros to perform custom processing on templates](template-macros.md)
+ [Using modules to encapsulate and reuse resource configurations](modules.md)
+ [Perform ECS blue/green deployments through CodeDeploy using AWS CloudFormation](blue-green.md)
+ [Using regular expressions in AWS CloudFormation templates](cfn-regexes.md)