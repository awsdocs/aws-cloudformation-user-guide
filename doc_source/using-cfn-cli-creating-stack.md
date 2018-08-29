# Creating a Stack<a name="using-cfn-cli-creating-stack"></a>

To create a stack you run the `[aws cloudformation create\-stack](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html)` command\. You must provide the stack name, the location of a valid template, and any input parameters\.

Parameters are separated with a space and the key names are case sensitive\. If you mistype a parameter key name when you run `aws cloudformation create-stack`, AWS CloudFormation doesn't create the stack and reports that the template doesn't contain that parameter\.

**Note**  
If you specify a local template file, AWS CloudFormation uploads it to an Amazon S3 bucket in your AWS account\. AWS CloudFormation creates a unique bucket for each region in which you upload a template file\. The buckets are accessible to anyone with Amazon S3 permissions in your AWS account\. If an AWS CloudFormation\-created bucket already exists, the template is added to that bucket\.  
You can use your own bucket and manage its permissions by manually uploading templates to Amazon S3\. Then whenever you create or update a stack, specify the Amazon S3 URL of a template file\.

By default, `aws cloudformation describe-stacks` returns parameter values\. To prevent sensitive parameter values such as passwords from being returned, include a `NoEcho` property set to `TRUE` in your AWS CloudFormation template\.

The following example creates the `myteststack` stack:

```
1. PROMPT> aws cloudformation create-stack --stack-name myteststack --template-body file:///home/testuser/mytemplate.json --parameters ParameterKey=Parm1,ParameterValue=test1 ParameterKey=Parm2,ParameterValue=test2
2. {
3.   "StackId" : "arn:aws:cloudformation:us-west-2:123456789012:stack/myteststack/330b0120-1771-11e4-af37-50ba1b98bea6"
4. }
```