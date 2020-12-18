# Retrieving a template<a name="using-cfn-get-template"></a>

AWS CloudFormation stores the template you use to create your stack as part of the stack\. You can retrieve the template from AWS CloudFormation using the [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/get-template.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/get-template.html) command\.

**Note**  
The `aws cloudformation get-template` command returns the deleted stacks templates for up to 90 days after the stack has been deleted\.

The following example shows the template for the `myteststack` stack:

```
 1. PROMPT> aws cloudformation get-template --stack-name myteststack
 2. {
 3.     "TemplateBody": {
 4.         "AWSTemplateFormatVersion": "2010-09-09",
 5.         "Outputs": {
 6.             "BucketName": {
 7.                 "Description": "Name of S3 bucket to hold website content",
 8.                 "Value": {
 9.                     "Ref": "S3Bucket"
10.                 }
11.             }
12.         },
13.         "Description": "AWS CloudFormation Sample Template S3_Bucket: Sample template showing how to create a publicly accessible S3 bucket. **WARNING** This template creates an S3 bucket.
14. You will be billed for the AWS resources used if you create a stack from this template.",
15.         "Resources": {
16.             "S3Bucket": {
17.                 "Type": "AWS::S3::Bucket",
18.                 "Properties": {
19.                     "AccessControl": "PublicRead"
20.                 }
21.             }
22.         }
23.     }
24. }
```

The output contains the entire template body, enclosed in quotation marks\.