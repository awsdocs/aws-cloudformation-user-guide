# Retrieving a Template<a name="using-cfn-get-template"></a>

AWS CloudFormation stores the template you use to create your stack as part of the stack\. You can retrieve the template from AWS CloudFormation using the [http://docs.aws.amazon.com/cli/latest/reference/cloudformation/get-template.html](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/get-template.html) command\.

**Note**  
The `aws cloudformation get-template` command returns the deleted stacks templates for up to 90 days after the stack has been deleted\.

The following example shows the template for the `myteststack` stack:

```
 PROMPT> aws cloudformation get-template --stack-name myteststack

 {
     "TemplateBody": {
         "AWSTemplateFormatVersion": "2010-09-09",
         "Outputs": {
             "BucketName": {
                 "Description": "Name of S3 bucket to hold website content",
                 "Value": {
                     "Ref": "S3Bucket"
                 }
             }
         },
         "Description": "AWS CloudFormation Sample Template S3_Bucket: Sample template showing how to create a publicly accessible S3 bucket. **WARNING** This template creates an S3 bucket.
 You will be billed for the AWS resources used if you create a stack from this template.",
         "Resources": {
             "S3Bucket": {
                 "Type": "AWS::S3::Bucket",
                 "Properties": {
                     "AccessControl": "PublicRead"
                 }
             }
         }
     }
 }
```

The output contains the entire template body, enclosed in quotation marks\.