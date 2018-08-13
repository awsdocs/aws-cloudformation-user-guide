# AWS CodeBuild Project Source<a name="aws-properties-codebuild-project-source"></a>

`Source` is a property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource that specifies the source code settings for an AWS CodeBuild project\.

## Syntax<a name="aws-properties-codebuild-project-source-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-source-syntax.json"></a>

```
{
  "[Auth](#cfn-codebuild-project-source-auth)" : [*SourceAuth*](aws-properties-codebuild-project-sourceauth.md),
  "[BuildSpec](#cfn-codebuild-project-source-buildspec)" : String,
  "[GitCloneDepth](#cfn-codebuild-project-source-gitclonedepth)" : Integer,
  "[InsecureSsl](#cfn-codebuild-project-source-insecuressl)" : Boolean,
  "[Location](#cfn-codebuild-project-source-location)" : String,
  "[Type](#cfn-codebuild-project-source-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-source-syntax.yaml"></a>

```
[Auth](#cfn-codebuild-project-source-auth): 
  [*SourceAuth*](aws-properties-codebuild-project-sourceauth.md)
[BuildSpec](#cfn-codebuild-project-source-buildspec): String
[GitCloneDepth](#cfn-codebuild-project-source-gitclonedepth): Integer
[InsecureSsl](#cfn-codebuild-project-source-insecuressl): Boolean
[Location](#cfn-codebuild-project-source-location): String
[Type](#cfn-codebuild-project-source-type): String
```

## Properties<a name="w3ab2c21c14d371b7"></a>

`Auth`  <a name="cfn-codebuild-project-source-auth"></a>
Information about the authorization settings for AWS CodeBuild to access the source code to be built\.  
Your code shouldn't get or set this information directly unless the project's source type is `GITHUB`\.
 *Required*: No  
 *Type*: [AWS CodeBuild Project SourceAuth](aws-properties-codebuild-project-sourceauth.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`BuildSpec`  <a name="cfn-codebuild-project-source-buildspec"></a>
The build specification for the project\. If this value is not provided, then the source code must contain a build spec file named `buildspec.yml` at the root level\. If this value is provided, it can be either a single string containing the entire build specification, or the path to an alternate build spec file relative to the value of the built\-in environment variable `CODEBUILD_SRC_DIR`\. The alternate build spec file can have a name other than `buildspec.yml`, for example `myspec.yml` or `build_spec_qa.yml` or similar\. For more information, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html#build-spec-ref-example](http://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html#build-spec-ref-example) in the *AWS CodeBuild User Guide*\.  
*Required*: No  
*Type*: String

`GitCloneDepth`  <a name="cfn-codebuild-project-source-gitclonedepth"></a>
The depth of history to download\. Minimum value is 0\. If this value is 0, greater than 25, or not provided, then the full history is downloaded with each build project\. If your source type is Amazon S3, this value is not supported\.  
*Required*: No  
*Type*: Integer

`InsecureSsl`  <a name="cfn-codebuild-project-source-insecuressl"></a>
This is used with GitHub Enterprise only\. Set to `true` to ignore SSL warnings while connecting to your GitHub Enterprise project repository\. The default value is `false`\. `InsecureSsl` should be used for testing purposes only\. It should not be used in a production environment\.  
*Required*: No  
*Type*: Boolean

`Location`  <a name="cfn-codebuild-project-source-location"></a>
The location of the source code in the specified repository type\. For more information, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: Conditional\. If you specify `CODEPIPELINE` for the `Type` property, don't specify this property\. For all of the other types, you must specify this property\.  
*Type*: String

`Type`  <a name="cfn-codebuild-project-source-type"></a>
The type of repository that contains your source code\. For valid values, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required*: Yes  
*Type*: String