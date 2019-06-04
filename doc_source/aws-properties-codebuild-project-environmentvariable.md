# AWS::CodeBuild::Project EnvironmentVariable<a name="aws-properties-codebuild-project-environmentvariable"></a>

 `EnvironmentVariable` is a property of the [AWS CodeBuild Project Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-environment.html) property type that specifies the name and value of an environment variable for an AWS CodeBuild project environment\. When you use the environment to run a build, these variables are available for your builds to use\. `EnvironmentVariable` contains a list of `EnvironmentVariable` property types\.

## Syntax<a name="aws-properties-codebuild-project-environmentvariable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-environmentvariable-syntax.json"></a>

```
{
  "[Name](#cfn-codebuild-project-environmentvariable-name)" : String,
  "[Type](#cfn-codebuild-project-environmentvariable-type)" : String,
  "[Value](#cfn-codebuild-project-environmentvariable-value)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-environmentvariable-syntax.yaml"></a>

```
  [Name](#cfn-codebuild-project-environmentvariable-name): String
  [Type](#cfn-codebuild-project-environmentvariable-type): String
  [Value](#cfn-codebuild-project-environmentvariable-value): String
```

## Properties<a name="aws-properties-codebuild-project-environmentvariable-properties"></a>

`Name`  <a name="cfn-codebuild-project-environmentvariable-name"></a>
The name or key of the environment variable\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codebuild-project-environmentvariable-type"></a>
The type of environment variable\. Valid values include:  
+  `PARAMETER_STORE`: An environment variable stored in Amazon EC2 Systems Manager Parameter Store\.
+  `PLAINTEXT`: An environment variable in plaintext format\.
*Required*: No  
*Type*: String  
*Allowed Values*: `PARAMETER_STORE | PLAINTEXT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-codebuild-project-environmentvariable-value"></a>
The value of the environment variable\.  
We strongly discourage the use of environment variables to store sensitive values, especially AWS secret key IDs and secret access keys\. Environment variables can be displayed in plain text using the AWS CodeBuild console and the AWS Command Line Interface \(AWS CLI\)\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)