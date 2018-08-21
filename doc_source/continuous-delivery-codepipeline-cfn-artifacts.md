# AWS CloudFormation Artifacts<a name="continuous-delivery-codepipeline-cfn-artifacts"></a>

AWS CodePipeline performs tasks on artifacts as AWS CodePipeline runs a pipeline\. For AWS CloudFormation, artifacts can include a stack template file, a template configuration file, or both\. AWS CodePipeline uses these artifacts to work with AWS CloudFormation stacks and change sets\.

If you use Amazon Simple Storage Service \(Amazon S3\) as a source repository, you must zip the template and template configuration files into a single file before you upload them to an S3 bucket\. For other repositories, such as GitHub and AWS CodeCommit, upload artifacts without zipping them\. For more information, see [Create a Pipeline in AWS CodePipeline](http://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-pipelines.html) in the *AWS CodePipeline User Guide*\.

You can add as many files as you need to your repository\. For example, you might want to include two different configurations for the same template: one for a test configuration and another for a production configuration\.

This topic describes each artifact type\.

**Topics**
+ [Stack Template File](#w3ab2c13c15c13)
+ [Template Configuration File](#w3ab2c13c15c15)

## Stack Template File<a name="w3ab2c13c15c13"></a>

A stack template file defines the resources that AWS CloudFormation provisions and configures\. These files are the same templates files that you use when you create or update stacks using AWS CloudFormation\. You can use YAML or JSON\-formatted templates\. For more information about templates, see [Template Anatomy](template-anatomy.md)\.

## Template Configuration File<a name="w3ab2c13c15c15"></a>

A template configuration file is a JSON\-formatted text file that can specify template parameter values, a [stack policy](protect-stack-resources.md), and tags\. Use these configuration files to specify parameter values or a stack policy for a stack\. All of the parameter values that you specify must be declared in the associated template\.

If you include sensitive information—such as passwords—in this file, restrict access to it\. For example, if you upload your artifact to an S3 bucket, use [S3 bucket policies or user policies](http://docs.aws.amazon.com/AmazonS3/latest/dev/using-iam-policies.html) to restrict access\.

To create a configuration file, use the following format :

```
{
  "Parameters" : {
    "NameOfTemplateParameter" : "ValueOfParameter",
    ...
  },
  "Tags" : {
    "TagKey" : "TagValue",
    ...
  }, 
  "StackPolicy" : {
    "Statement" : [
      StackPolicyStatement
    ]
  }
}
```

The following example specifies `TestEC2Key` for the `KeyName` parameter, adds a `Department` tag whose value is `Marketing`, and adds a stack policy that allows all update actions except for an update that deletes a resource\.

```
{
  "Parameters" : {
    "KeyName" : "TestEC2Key"
  },
  "Tags" : {
    "Department" : "Marketing"
  },
  "StackPolicy" : {
    "Statement" : [
      {
        "Effect" : "Allow",
        "NotAction" : "Update:Delete",
        "Principal": "*",
        "Resource" : "*"
      }
    ]
  }
}
```