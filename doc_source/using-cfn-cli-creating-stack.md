# Creating a stack<a name="using-cfn-cli-creating-stack"></a>

To create a stack you run the `[aws cloudformation create\-stack](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html)` command\. You must provide the stack name, the location of a valid template, and any input parameters\.

Parameters are separated with a space and the key names are case sensitive\. If you mistype a parameter key name when you run `aws cloudformation create-stack`, AWS CloudFormation doesn't create the stack and reports that the template doesn't contain that parameter\.

**Note**  
You can use your own bucket and manage its permissions by manually uploading templates to Amazon S3\. Then whenever you create or update a stack, specify the Amazon S3 URL of a template file\.

By default, `aws cloudformation describe-stacks` returns parameter values\. To prevent sensitive parameter values such as passwords from being returned, include a `NoEcho` property set to `TRUE` in your AWS CloudFormation template\.

**Important**  
Using the `NoEcho` attribute does not mask any information stored in the following:  
The `Metadata` template section\. CloudFormation does not transform, modify, or redact any information you include in the `Metadata` section\. For more information, see [Metadata](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)\.
The `Outputs` template section\. For more information, see [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)\.
The `Metadata` attribute of a resource definition\. For more information, [Metadata attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-metadata.html)\.
We strongly recommend you do not use these mechanisms to include sensitive information, such as passwords or secrets\.

**Important**  
Rather than embedding sensitive information directly in your AWS CloudFormation templates, we recommend you use dynamic parameters in the stack template to reference sensitive information that is stored and managed outside of CloudFormation, such as in the AWS Systems Manager Parameter Store or AWS Secrets Manager\.  
For more information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

The following example creates the `myteststack` stack:

```
1. PROMPT> aws cloudformation create-stack --stack-name myteststack --template-body file:///home/testuser/mytemplate.json --parameters ParameterKey=Parm1,ParameterValue=test1 ParameterKey=Parm2,ParameterValue=test2
2. {
3.   "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/myteststack/330b0120-1771-11e4-af37-50ba1b98bea6"
4. }
```