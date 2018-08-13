# Working with AWS CloudFormation Templates<a name="template-guide"></a>

To provision and configure your stack resources, you must understand AWS CloudFormation templates, which are formatted text files in JSON or YAML\. These templates describe the resources that you want to provision in your AWS CloudFormation stacks\. You can use AWS CloudFormation Designer or any text editor to create and save templates\. For information about the structure and syntax of a template, see [Template Anatomy](template-anatomy.md)\.

If you're unfamiliar with JSON or YAML, you can use AWS CloudFormation Designer to help you get started with AWS CloudFormation templates\. AWS CloudFormation Designer is a tool for visually creating and modifying templates\. For more information, see [What Is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)\.

[Template Snippets](CHAP_TemplateQuickRef.md) provides examples that demonstrate how to write templates for a particular resource\. For example, you can view snippets for Amazon EC2 instances, Amazon S3 domains, AWS CloudFormation mappings, and more\. Snippets are grouped by resource, with general\-purpose AWS CloudFormation snippets in [General Template Snippets](quickref-general.md)\.

For details about the supported resources, type names, intrinsic functions, and pseudo parameters you can use in your templates, see [Template Reference](template-reference.md)\.

**Topics**
+ [AWS CloudFormation Template Formats](template-formats.md)
+ [Template Anatomy](template-anatomy.md)
+ [What Is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)
+ [Walkthroughs](CHAP_Using.md)
+ [Template Snippets](CHAP_TemplateQuickRef.md)
+ [Custom Resources](template-custom-resources.md)
+ [Using Regular Expressions in AWS CloudFormation Templates](cfn-regexes.md)
+ [Using CloudFormer to Create AWS CloudFormation Templates from Existing AWS Resources](cfn-using-cloudformer.md)