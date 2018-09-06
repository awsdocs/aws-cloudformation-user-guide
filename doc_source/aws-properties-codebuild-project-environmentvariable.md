# AWS CodeBuild Project EnvironmentVariable<a name="aws-properties-codebuild-project-environmentvariable"></a>

The `EnvironmentVariable` property type specifies the name and value of an environment variable for an AWS CodeBuild project environment\. When you use the environment to run a build, these variables are available for your builds to use\.

The `EnvironmentVariables` property of the [AWS CodeBuild Project Environment](aws-properties-codebuild-project-environment.md) property type contains a list of `EnvironmentVariable` property types\.

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

## Properties<a name="w3ab2c21c14d367b9"></a>

`Name`  <a name="cfn-codebuild-project-environmentvariable-name"></a>
The name of an environment variable\.  
*Required*: Yes  
*Type*: String

`Type`  <a name="cfn-codebuild-project-environmentvariable-type"></a>
The type of environment variable\. Valid values are:  
+ `PARAMETER_STORE`: An environment variable stored in Systems Manager Parameter Store\.
+ `PLAINTEXT`: An environment variable in plaintext format\.
*Required: *No  
*Type*: String

`Value`  <a name="cfn-codebuild-project-environmentvariable-value"></a>
The value of the environment variable\.  
*Required*: Yes  
*Type*: String