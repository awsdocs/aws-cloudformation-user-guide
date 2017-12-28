# AWS CodeBuild Project Environment<a name="aws-properties-codebuild-project-environment"></a>

`Environment` is a property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource that specifies the environment for an AWS CodeBuild project\.

## Syntax<a name="aws-properties-codebuild-project-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-environment-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-computetype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-environmentvariables)" : [ EnvironmentVariable ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-image)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-privilegedmode)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-environment-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-computetype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-environmentvariables):
  - EnvironmentVariable
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-image): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-privilegedmode): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-environment-type): String
```

## Properties<a name="w3ab2c21c14d293b7"></a>

`ComputeType`  
The type of compute environment, such as `BUILD_GENERAL1_SMALL`\. The compute type determines the number of CPU cores and memory the build environment uses\. For valid values, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required: *Yes  
*Type*: String

`EnvironmentVariables`  
The environment variables that your builds can use\. For more information, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required: *No  
*Type*: List of [AWS CodeBuild Project EnvironmentVariable](aws-properties-codebuild-project-environmentvariable.md)

`Image`  
The Docker image identifier that the build environment uses\. For more information, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required: *Yes  
*Type*: String

`PrivilegedMode`  
Indicates how the project builds Docker images\. Specify `true` to enable running the Docker daemon inside a Docker container\.  
This value must be set to `true` only if this build project will be used to build Docker images, and the specified build environment image is not one provided by AWS CodeBuild with Docker support\. Otherwise, all associated builds that attempt to interact with the Docker daemon will fail\. For more information, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required: *No  
*Type*: Boolean

`Type`  
The type of build environment\. For valid values, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required: *Yes  
*Type*: String