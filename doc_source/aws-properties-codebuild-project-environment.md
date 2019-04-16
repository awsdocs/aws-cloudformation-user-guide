# AWS CodeBuild Project Environment<a name="aws-properties-codebuild-project-environment"></a>

`Environment` is a property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource that specifies the environment for an AWS CodeBuild project\.

## Syntax<a name="aws-properties-codebuild-project-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-environment-syntax.json"></a>

```
{
  "[Certificate](#cfn-codebuild-project-environment-certificate)" : String,
  "[ComputeType](#cfn-codebuild-project-environment-computetype)" : String,
  "[EnvironmentVariables](#cfn-codebuild-project-environment-environmentvariables)" : [ [EnvironmentVariable](aws-properties-codebuild-project-environmentvariable.md) ],
  "[Image](#cfn-codebuild-project-environment-image)" : String,
  "[ImagePullCredentialsType](#cfn-codebuild-project-environment-imagepullcredentialstype)" : String,
  "[PrivilegedMode](#cfn-codebuild-project-environment-privilegedmode)" : Boolean,
  "[RegistryCredential](#cfn-codebuild-project-environment-registrycredential)" : [RegistryCredential](aws-properties-codebuild-project-registrycredential.md),        
  "[Type](#cfn-codebuild-project-environment-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-environment-syntax.yaml"></a>

```
[Certificate](#cfn-codebuild-project-environment-certificate): String
[ComputeType](#cfn-codebuild-project-environment-computetype): String
[EnvironmentVariables](#cfn-codebuild-project-environment-environmentvariables):
  - [EnvironmentVariable](aws-properties-codebuild-project-environmentvariable.md)
[Image](#cfn-codebuild-project-environment-image): String
[ImagePullCredentialsType](#cfn-codebuild-project-environment-imagepullcredentialstype): String
[RegistryCredential](#cfn-codebuild-project-environment-registrycredential): [RegistryCredential](aws-properties-codebuild-project-registrycredential.md)
[PrivilegedMode](#cfn-codebuild-project-environment-privilegedmode): Boolean
[Type](#cfn-codebuild-project-environment-type): String
```

## Properties<a name="w13ab1c21c10c72c13c23b7"></a>

`Certificate`  <a name="cfn-codebuild-project-environment-certificate"></a>
The certificate to use with the build project\.  
*Required*: No  
*Type*: String

`ComputeType`  <a name="cfn-codebuild-project-environment-computetype"></a>
The type of compute environment, such as `BUILD_GENERAL1_SMALL`\. The compute type determines the number of CPU cores and memory the build environment uses\. For valid values, see the [https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: Yes  
*Type*: String

`EnvironmentVariables`  <a name="cfn-codebuild-project-environment-environmentvariables"></a>
The environment variables that your builds can use\. For more information, see the [https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: No  
*Type*: List of [EnvironmentVariable](aws-properties-codebuild-project-environmentvariable.md)

`Image`  <a name="cfn-codebuild-project-environment-image"></a>
The image tag or image digest that identifies the Docker image to use for this build project\. Use the following formats:  
+ For an image tag: `registry/repository:tag`\. For example, to specify an image with the tag "latest," use `registry/repository:latest`\.
+ For an image digest: `registry/repository@digest`\. For example, to specify an image with the digest "sha256:cbbf2f9a99b47fc460d422812b6a5adff7dfee951d8fa2e4a98caa0382cfbdbf," use `registry/repository@sha256:cbbf2f9a99b47fc460d422812b6a5adff7dfee951d8fa2e4a98caa0382cfbdbf`\.
For more information, see the [https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: Yes  
*Type*: String

`ImagePullCredentialsType`  <a name="cfn-codebuild-project-environment-imagepullcredentialstype"></a>
 The type of credentials AWS CodeBuild uses to pull images in your build\. There are two valid values:   
+  `CODEBUILD` specifies that AWS CodeBuild uses its own credentials\. This requires that you modify your ECR repository policy to trust the AWS CodeBuild service principal\. 
+  `SERVICE_ROLE` specifies that AWS CodeBuild uses your build project's service role\. 
 When you use a cross\-account or private registry image, you must use `SERVICE_ROLE` credentials\. When you use an AWS CodeBuild curated image, you must use `CODEBUILD` credentials\.   
 The Docker image identifier that the build environment uses\. For more information, see the [https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: Yes  
*Type*: String

`PrivilegedMode`  <a name="cfn-codebuild-project-environment-privilegedmode"></a>
Indicates how the project builds Docker images\. Specify `true` to enable running the Docker daemon inside a Docker container\.  
This value must be set to `true` only if this build project will be used to build Docker images, and the specified build environment image is not one provided by AWS CodeBuild with Docker support\. Otherwise, all associated builds that attempt to interact with the Docker daemon will fail\. For more information, see the [https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: No  
*Type*: Boolean

`RegistryCredential`  <a name="cfn-codebuild-project-environment-registrycredential"></a>
 `RegistryCredential` is a property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource that specifies information about credentials that provide access to a private Docker registry\. When this is set:   
+  `imagePullCredentialsType` must be set to `SERVICE_ROLE`\. 
+  images cannot be curated or an Amazon ECR image\. 
 For more information, see the [https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: No  
*Type*: [RegistryCredential](aws-properties-codebuild-project-registrycredential.md)

`Type`  <a name="cfn-codebuild-project-environment-type"></a>
The type of build environment\. For valid values, see the [https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: Yes  
*Type*: String