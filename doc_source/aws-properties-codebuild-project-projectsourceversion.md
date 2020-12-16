# AWS::CodeBuild::Project ProjectSourceVersion<a name="aws-properties-codebuild-project-projectsourceversion"></a>

 A source identifier and its corresponding version\. 

## Syntax<a name="aws-properties-codebuild-project-projectsourceversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-projectsourceversion-syntax.json"></a>

```
{
  "[SourceIdentifier](#cfn-codebuild-project-projectsourceversion-sourceidentifier)" : String,
  "[SourceVersion](#cfn-codebuild-project-projectsourceversion-sourceversion)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-projectsourceversion-syntax.yaml"></a>

```
  [SourceIdentifier](#cfn-codebuild-project-projectsourceversion-sourceidentifier): String
  [SourceVersion](#cfn-codebuild-project-projectsourceversion-sourceversion): String
```

## Properties<a name="aws-properties-codebuild-project-projectsourceversion-properties"></a>

`SourceIdentifier`  <a name="cfn-codebuild-project-projectsourceversion-sourceidentifier"></a>
An identifier for a source in the build project\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceVersion`  <a name="cfn-codebuild-project-projectsourceversion-sourceversion"></a>
The source version for the corresponding source identifier\. If specified, must be one of:  
+ For AWS CodeCommit: the commit ID, branch, or Git tag to use\.
+ For GitHub: the commit ID, pull request ID, branch name, or tag name that corresponds to the version of the source code you want to build\. If a pull request ID is specified, it must use the format `pr/pull-request-ID` \(for example, `pr/25`\)\. If a branch name is specified, the branch's HEAD commit ID is used\. If not specified, the default branch's HEAD commit ID is used\.
+ For Bitbucket: the commit ID, branch name, or tag name that corresponds to the version of the source code you want to build\. If a branch name is specified, the branch's HEAD commit ID is used\. If not specified, the default branch's HEAD commit ID is used\.
+ For Amazon Simple Storage Service \(Amazon S3\): the version ID of the object that represents the build input ZIP file to use\.
 For more information, see [Source Version Sample with CodeBuild](https://docs.aws.amazon.com/codebuild/latest/userguide/sample-source-version.html) in the *AWS CodeBuild User Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)