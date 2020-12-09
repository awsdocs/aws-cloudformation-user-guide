# AWS::CodeBuild::Project Source<a name="aws-properties-codebuild-project-source"></a>

 `Source` is a property of the [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html) resource that specifies the source code settings for the project, such as the source code's repository type and location\. 

## Syntax<a name="aws-properties-codebuild-project-source-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-source-syntax.json"></a>

```
{
  "[Auth](#cfn-codebuild-project-source-auth)" : SourceAuth,
  "[BuildSpec](#cfn-codebuild-project-source-buildspec)" : String,
  "[BuildStatusConfig](#cfn-codebuild-project-source-buildstatusconfig)" : BuildStatusConfig,
  "[GitCloneDepth](#cfn-codebuild-project-source-gitclonedepth)" : Integer,
  "[GitSubmodulesConfig](#cfn-codebuild-project-source-gitsubmodulesconfig)" : GitSubmodulesConfig,
  "[InsecureSsl](#cfn-codebuild-project-source-insecuressl)" : Boolean,
  "[Location](#cfn-codebuild-project-source-location)" : String,
  "[ReportBuildStatus](#cfn-codebuild-project-source-reportbuildstatus)" : Boolean,
  "[SourceIdentifier](#cfn-codebuild-project-source-sourceidentifier)" : String,
  "[Type](#cfn-codebuild-project-source-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-source-syntax.yaml"></a>

```
  [Auth](#cfn-codebuild-project-source-auth): 
    SourceAuth
  [BuildSpec](#cfn-codebuild-project-source-buildspec): String
  [BuildStatusConfig](#cfn-codebuild-project-source-buildstatusconfig): 
    BuildStatusConfig
  [GitCloneDepth](#cfn-codebuild-project-source-gitclonedepth): Integer
  [GitSubmodulesConfig](#cfn-codebuild-project-source-gitsubmodulesconfig): 
    GitSubmodulesConfig
  [InsecureSsl](#cfn-codebuild-project-source-insecuressl): Boolean
  [Location](#cfn-codebuild-project-source-location): String
  [ReportBuildStatus](#cfn-codebuild-project-source-reportbuildstatus): Boolean
  [SourceIdentifier](#cfn-codebuild-project-source-sourceidentifier): String
  [Type](#cfn-codebuild-project-source-type): String
```

## Properties<a name="aws-properties-codebuild-project-source-properties"></a>

`Auth`  <a name="cfn-codebuild-project-source-auth"></a>
Information about the authorization settings for AWS CodeBuild to access the source code to be built\.  
This information is for the AWS CodeBuild console's use only\. Your code should not get or set `Auth` directly\.  
*Required*: No  
*Type*: [SourceAuth](aws-properties-codebuild-project-sourceauth.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BuildSpec`  <a name="cfn-codebuild-project-source-buildspec"></a>
The build specification for the project\. If this value is not provided, then the source code must contain a buildspec file named `buildspec.yml` at the root level\. If this value is provided, it can be either a single string containing the entire build specification, or the path to an alternate buildspec file relative to the value of the built\-in environment variable `CODEBUILD_SRC_DIR`\. The alternate buildspec file can have a name other than `buildspec.yml`, for example `myspec.yml` or `build_spec_qa.yml` or similar\. For more information, see the [Build Spec Reference](https://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html#build-spec-ref-example) in the *AWS CodeBuild User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BuildStatusConfig`  <a name="cfn-codebuild-project-source-buildstatusconfig"></a>
Contains information that defines how the build project reports the build status to the source provider\. This option is only used when the source provider is `GITHUB`, `GITHUB_ENTERPRISE`, or `BITBUCKET`\.  
*Required*: No  
*Type*: [BuildStatusConfig](aws-properties-codebuild-project-buildstatusconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GitCloneDepth`  <a name="cfn-codebuild-project-source-gitclonedepth"></a>
 The depth of history to download\. Minimum value is 0\. If this value is 0, greater than 25, or not provided, then the full history is downloaded with each build project\. If your source type is Amazon S3, this value is not supported\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GitSubmodulesConfig`  <a name="cfn-codebuild-project-source-gitsubmodulesconfig"></a>
 Information about the Git submodules configuration for the build project\.   
*Required*: No  
*Type*: [GitSubmodulesConfig](aws-properties-codebuild-project-gitsubmodulesconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsecureSsl`  <a name="cfn-codebuild-project-source-insecuressl"></a>
 This is used with GitHub Enterprise only\. Set to true to ignore SSL warnings while connecting to your GitHub Enterprise project repository\. The default value is `false`\. `InsecureSsl` should be used for testing purposes only\. It should not be used in a production environment\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Location`  <a name="cfn-codebuild-project-source-location"></a>
Information about the location of the source code to be built\. Valid values include:  
+ For source code settings that are specified in the source action of a pipeline in AWS CodePipeline, `location` should not be specified\. If it is specified, AWS CodePipeline ignores it\. This is because AWS CodePipeline uses the settings in a pipeline's source action instead of this value\.
+ For source code in an AWS CodeCommit repository, the HTTPS clone URL to the repository that contains the source code and the build spec \(for example, `https://git-codecommit.region-ID.amazonaws.com/v1/repos/repo-name `\)\.
+ For source code in an Amazon Simple Storage Service \(Amazon S3\) input bucket, one of the following\. 
  +  The path to the ZIP file that contains the source code \(for example, ` bucket-name/path/to/object-name.zip`\)\. 
  +  The path to the folder that contains the source code \(for example, ` bucket-name/path/to/source-code/folder/`\)\. 
+ For source code in a GitHub repository, the HTTPS clone URL to the repository that contains the source and the build spec\. You must connect your AWS account to your GitHub account\. Use the AWS CodeBuild console to start creating a build project\. When you use the console to connect \(or reconnect\) with GitHub, on the GitHub **Authorize application** page, for **Organization access**, choose **Request access** next to each repository you want to allow AWS CodeBuild to have access to, and then choose **Authorize application**\. \(After you have connected to your GitHub account, you do not need to finish creating the build project\. You can leave the AWS CodeBuild console\.\) To instruct AWS CodeBuild to use this connection, in the `source` object, set the `auth` object's `type` value to `OAUTH`\.
+ For source code in a Bitbucket repository, the HTTPS clone URL to the repository that contains the source and the build spec\. You must connect your AWS account to your Bitbucket account\. Use the AWS CodeBuild console to start creating a build project\. When you use the console to connect \(or reconnect\) with Bitbucket, on the Bitbucket **Confirm access to your account** page, choose **Grant access**\. \(After you have connected to your Bitbucket account, you do not need to finish creating the build project\. You can leave the AWS CodeBuild console\.\) To instruct AWS CodeBuild to use this connection, in the `source` object, set the `auth` object's `type` value to `OAUTH`\.
 If you specify `CODEPIPELINE` for the `Type` property, don't specify this property\. For all of the other types, you must specify `Location`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportBuildStatus`  <a name="cfn-codebuild-project-source-reportbuildstatus"></a>
 Set to true to report the status of a build's start and finish to your source provider\. This option is valid only when your source provider is GitHub, GitHub Enterprise, or Bitbucket\. If this is set and you use a different source provider, an `invalidInputException` is thrown\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceIdentifier`  <a name="cfn-codebuild-project-source-sourceidentifier"></a>
 An identifier for this project source\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codebuild-project-source-type"></a>
The type of repository that contains the source code to be built\. Valid values include:  
+  `BITBUCKET`: The source code is in a Bitbucket repository\.
+  `CODECOMMIT`: The source code is in an AWS CodeCommit repository\.
+  `CODEPIPELINE`: The source code settings are specified in the source action of a pipeline in AWS CodePipeline\.
+  `GITHUB`: The source code is in a GitHub or GitHub Enterprise Cloud repository\.
+  `GITHUB_ENTERPRISE`: The source code is in a GitHub Enterprise Server repository\.
+  `NO_SOURCE`: The project does not have input source code\.
+  `S3`: The source code is in an Amazon Simple Storage Service \(Amazon S3\) input bucket\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `BITBUCKET | CODECOMMIT | CODEPIPELINE | GITHUB | GITHUB_ENTERPRISE | NO_SOURCE | S3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)