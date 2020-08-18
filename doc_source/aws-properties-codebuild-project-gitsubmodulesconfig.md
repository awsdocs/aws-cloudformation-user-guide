# AWS::CodeBuild::Project GitSubmodulesConfig<a name="aws-properties-codebuild-project-gitsubmodulesconfig"></a>

 `GitSubmodulesConfig` is a property of the [AWS CodeBuild Project Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-source.html) property type that specifies information about the Git submodules configuration for the build project\. 

## Syntax<a name="aws-properties-codebuild-project-gitsubmodulesconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-gitsubmodulesconfig-syntax.json"></a>

```
{
  "[FetchSubmodules](#cfn-codebuild-project-gitsubmodulesconfig-fetchsubmodules)" : Boolean
}
```

### YAML<a name="aws-properties-codebuild-project-gitsubmodulesconfig-syntax.yaml"></a>

```
  [FetchSubmodules](#cfn-codebuild-project-gitsubmodulesconfig-fetchsubmodules): Boolean
```

## Properties<a name="aws-properties-codebuild-project-gitsubmodulesconfig-properties"></a>

`FetchSubmodules`  <a name="cfn-codebuild-project-gitsubmodulesconfig-fetchsubmodules"></a>
 Set to true to fetch Git submodules for your AWS CodeBuild build project\.   
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-codebuild-project-gitsubmodulesconfig--seealso"></a>
+  [ GitSubmodulesConfig](https://docs.aws.amazon.com/codebuild/latest/APIReference/API_GitSubmodulesConfig.html) in the *AWS CodeBuild API Reference* 