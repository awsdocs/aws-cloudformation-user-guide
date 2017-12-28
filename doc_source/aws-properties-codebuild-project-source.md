# AWS CodeBuild Project Source<a name="aws-properties-codebuild-project-source"></a>

`Source` is a property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource that specifies the source code settings for an AWS CodeBuild project\.

## Syntax<a name="aws-properties-codebuild-project-source-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-source-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-source-auth)" : SourceAuth,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-source-buildspec)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-source-location)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-source-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-source-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-source-auth): 
  SourceAuth
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-source-buildspec): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-source-location): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-source-type): String
```

## Properties<a name="w3ab2c21c14d299b7"></a>

`Auth`  
Information about the authorization settings for AWS CodeBuild to access the source code to be built\.  
Your code shouldn't get or set this information directly unless the project's source type is `GITHUB`\.
 *Required*: No  
 *Type*: [AWS CodeBuild Project SourceAuth](aws-properties-codebuild-project-sourceauth.md)  
 *Update requires*: No interruption 

`BuildSpec`  
The build specification for the project\. If this value is not provided, then the source code must contain a build spec file named `buildspec.yml` at the root level\. If this value is provided, it can be either a single string containing the entire build specification, or the path to an alternate build spec file relative to the value of the built\-in environment variable `CODEBUILD_SRC_DIR`\. The alternate build spec file can have a name other than `buildspec.yml`, for example `myspec.yml` or `build_spec_qa.yml` or similar\. For more information, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html#build-spec-ref-example](http://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html#build-spec-ref-example) in the *AWS CodeBuild User Guide*\.  
*Required: *No  
*Type*: String

`Location`  
The location of the source code in the specified repository type\. For more information, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required: *Conditional\. If you specify `CODEPIPELINE` for the `Type` property, don't specify this property\. For all of the other types, you must specify this property\.  
*Type*: String

`Type`  
The type of repository that contains your source code\. For valid values, see the [http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli](http://docs.aws.amazon.com/codebuild/latest/userguide/create-project.html#create-project-cli) field in the *AWS CodeBuild User Guide*\.  
*Required: *Yes  
*Type*: String