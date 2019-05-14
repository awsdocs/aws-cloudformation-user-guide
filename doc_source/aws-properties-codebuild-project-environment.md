# AWS::CodeBuild::Project Environment<a name="aws-properties-codebuild-project-environment"></a>

 `Environment` is a property of the [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html) resource that specifies the environment for an AWS CodeBuild project\. 

## Syntax<a name="aws-properties-codebuild-project-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-environment-syntax.json"></a>

```
{
  "[Certificate](#cfn-codebuild-project-environment-certificate)" : String,
  "[ComputeType](#cfn-codebuild-project-environment-computetype)" : String,
  "[EnvironmentVariables](#cfn-codebuild-project-environment-environmentvariables)" : [ [EnvironmentVariable](aws-properties-codebuild-project-environmentvariable.md), ... ],
  "[Image](#cfn-codebuild-project-environment-image)" : String,
  "[ImagePullCredentialsType](#cfn-codebuild-project-environment-imagepullcredentialstype)" : String,
  "[PrivilegedMode](#cfn-codebuild-project-environment-privilegedmode)" : Boolean,
  "[RegistryCredential](#cfn-codebuild-project-environment-registrycredential)" : [RegistryCredential](aws-properties-codebuild-project-registrycredential.md),
  "[Type](#cfn-codebuild-project-environment-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-environment-syntax.yaml"></a>

```
﻿  [Certificate](#cfn-codebuild-project-environment-certificate) : String
﻿  [ComputeType](#cfn-codebuild-project-environment-computetype) : String
﻿  [EnvironmentVariables](#cfn-codebuild-project-environment-environmentvariables) : 
    - [EnvironmentVariable](aws-properties-codebuild-project-environmentvariable.md)
﻿  [Image](#cfn-codebuild-project-environment-image) : String
﻿  [ImagePullCredentialsType](#cfn-codebuild-project-environment-imagepullcredentialstype) : String
﻿  [PrivilegedMode](#cfn-codebuild-project-environment-privilegedmode) : Boolean
﻿  [RegistryCredential](#cfn-codebuild-project-environment-registrycredential) : 
    [RegistryCredential](aws-properties-codebuild-project-registrycredential.md)
﻿  [Type](#cfn-codebuild-project-environment-type) : String
```

## Properties<a name="aws-properties-codebuild-project-environment-properties"></a>

`Certificate`  <a name="cfn-codebuild-project-environment-certificate"></a>
The certificate to use with this build project\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComputeType`  <a name="cfn-codebuild-project-environment-computetype"></a>
The type of compute environment\. This determines the number of CPU cores and memory the build environment uses\. Available values include:  
+  `BUILD_GENERAL1_SMALL`: Use up to 3 GB memory and 2 vCPUs for builds\.
+  `BUILD_GENERAL1_MEDIUM`: Use up to 7 GB memory and 4 vCPUs for builds\.
+  `BUILD_GENERAL1_LARGE`: Use up to 15 GB memory and 8 vCPUs for builds\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentVariables`  <a name="cfn-codebuild-project-environment-environmentvariables"></a>
A set of environment variables to make available to builds for this build project\.  
*Required*: No  
*Type*: List of [EnvironmentVariable](aws-properties-codebuild-project-environmentvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Image`  <a name="cfn-codebuild-project-environment-image"></a>
The image tag or image digest that identifies the Docker image to use for this build project\. Use the following formats:  
+ For an image tag: `registry/repository:tag`\. For example, to specify an image with the tag "latest," use `registry/repository:latest`\.
+ For an image digest: `registry/repository@digest`\. For example, to specify an image with the digest "sha256:cbbf2f9a99b47fc460d422812b6a5adff7dfee951d8fa2e4a98caa0382cfbdbf," use `registry/repository@sha256:cbbf2f9a99b47fc460d422812b6a5adff7dfee951d8fa2e4a98caa0382cfbdbf`\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImagePullCredentialsType`  <a name="cfn-codebuild-project-environment-imagepullcredentialstype"></a>
 The type of credentials AWS CodeBuild uses to pull images in your build\. There are two valid values:   
+  `CODEBUILD` specifies that AWS CodeBuild uses its own credentials\. This requires that you modify your ECR repository policy to trust AWS CodeBuild's service principal\. 
+  `SERVICE_ROLE` specifies that AWS CodeBuild uses your build project's service role\. 
 When you use a cross\-account or private registry image, you must use SERVICE\_ROLE credentials\. When you use an AWS CodeBuild curated image, you must use CODEBUILD credentials\.   
*Required*: No  
*Type*: String  
*Allowed Values*: `CODEBUILD | SERVICE_ROLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivilegedMode`  <a name="cfn-codebuild-project-environment-privilegedmode"></a>
Indicates how the project builds Docker images\. Specify `true` to enable running the Docker daemon inside a Docker container\.  
This value must be set to `true` only if this build project will be used to build Docker images, and the specified build environment image is not one provided by AWS CodeBuild with Docker support\. Otherwise, all associated builds that attempt to interact with the Docker daemon fail\. For more information, see the [ `privilegedMode` ](https://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
You must also start the Docker daemon so that builds can interact with it\. One way to do this is to initialize the Docker daemon during the install phase of your build spec by running the following build commands\. \(Do not run these commands if the specified build environment image is provided by AWS CodeBuild with Docker support\.\)  
If the operating system's base image is Ubuntu Linux:  
 `- nohup /usr/local/bin/dockerd --host=unix:///var/run/docker.sock --host=tcp://0.0.0.0:2375 --storage-driver=overlay&`   
 `- timeout 15 sh -c "until docker info; do echo .; sleep 1; done"`   
If the operating system's base image is Alpine Linux, add the `-t` argument to `timeout`:  
 `- nohup /usr/local/bin/dockerd --host=unix:///var/run/docker.sock --host=tcp://0.0.0.0:2375 --storage-driver=overlay&`   
 `- timeout -t 15 sh -c "until docker info; do echo .; sleep 1; done"`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegistryCredential`  <a name="cfn-codebuild-project-environment-registrycredential"></a>
 `RegistryCredential` is a property of the [AWS::CodeBuild::Project Environment ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html#cfn-codebuild-project-environment) property that specifies information about credentials that provide access to a private Docker registry\. When this is set:  
+  `imagePullCredentialsType` must be set to `SERVICE_ROLE`\. 
+  images cannot be curated or an Amazon ECR image\. 
*Required*: No  
*Type*: [RegistryCredential](aws-properties-codebuild-project-registrycredential.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codebuild-project-environment-type"></a>
The type of build environment to use for related builds\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `LINUX_CONTAINER | WINDOWS_CONTAINER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)