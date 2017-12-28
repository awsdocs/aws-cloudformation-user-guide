# Selecting a Stack Template<a name="cfn-using-console-create-stack-template"></a>

After starting the Create Stack wizard, you specify the template that you want AWS CloudFormation to use to create your stack\.

AWS CloudFormation templates are JSON\- or YAML\-formatted files that specify the AWS resources that make up your stack\. For more information about AWS CloudFormation templates, see [Working with AWS CloudFormation Templates](template-guide.md)\.

**To choose a stack template:**

1. On the **Select Template** page, choose a stack template by using one of the following options:  
**Design a template**  
To create or modify a template, use AWS CloudFormation Designer, a drag\-and\-drop interface\. For more information, see [What Is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)\.  
**Choose a template**  

   + **Select a sample template\.**

     Select an AWS CloudFormation template from a list of samples\. For descriptions of the templates, see [Sample Templates](cfn-sample-templates.md)\.

     To create a stack from existing AWS resources by using the CloudFormer tool, select **CloudFormer** from the list\. For more information, see \.

   + **Upload a template to Amazon S3**\.

     Select an AWS CloudFormation template on your local computer\. Choose **Choose File** to select the template file that you want to upload\. The template can be a maximum size of 460,800 bytes\.

     If you use the CLI or API to create a stack, you can upload a template with a maximum size of 51,200 bytes\.
**Note**  
If you upload a local template file, AWS CloudFormation uploads it to an Amazon Simple Storage Service \(Amazon S3\) bucket in your AWS account\. The buckets are accessible to anyone with Amazon S3 permissions in your AWS account\. If you don't already have an S3 bucket that was created by AWS CloudFormation, it creates a unique bucket for each Region in which you upload a template file\. If you already have an S3 bucket that was created by AWS CloudFormation in your AWS account, AWS CloudFormation adds the template to that bucket\.  
You can use your own bucket and manage its permissions by manually uploading templates to Amazon S3\. When you create or update a stack, specify the Amazon S3 URL of a template file\.

   + **Specify an Amazon S3 template URL**\.

     Specify a URL to a template in an S3 bucket\.
**Important**  
If your template includes nested stacks \(for example, stacks described in other template documents located in subdirectories\), ensure that your S3 bucket contains the necessary files and directories\.

     If you have a template in a versioning\-enabled bucket, you can specify a specific version of the template, such as `https://s3.amazonaws.com/templates/myTemplate.template?versionId=123ab1cdeKdOW5IH4GAcYbEngcpTJTDW`\. For more information, see [Managing Objects in a Versioning\-Enabled Bucket](http://docs.aws.amazon.com/AmazonS3/latest/user-guide/managing-objects-versioned-bucket.html) in the *Amazon Simple Storage Service Console User Guide*\.

     The URL must point to a template with a maximum size of 460,800 bytes that is stored in an S3 bucket that you have read permissions to and that is located in the same region as the stack\. The URL can be a maximum of 1024 characters long\.

1. To accept your settings, choose **Next**, and proceed with specifying the stack name and parameters\.

   Before creating resources, AWS CloudFormation validates your template to catch syntactic and some semantic errors, such as circular dependencies\. During validation, AWS CloudFormation first checks if the template is valid JSON\. If it isn't, AWS CloudFormation checks if the template is valid YAML\. If both checks fail, AWS CloudFormation returns a template validation error\.