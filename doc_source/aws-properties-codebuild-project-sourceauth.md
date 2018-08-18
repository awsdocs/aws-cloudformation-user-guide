# AWS CodeBuild Project SourceAuth<a name="aws-properties-codebuild-project-sourceauth"></a>

The `SourceAuth` property type specifies authorization settings for AWS CodeBuild to access the source code to be built\.

 `SourceAuth` is a property of the [AWS CodeBuild Project Source](aws-properties-codebuild-project-source.md) property type\.

**Note**  
Your code shouldn't get or set this information directly unless the project's source type is `GITHUB`\.

## Syntax<a name="aws-properties-codebuild-project-sourceauth-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-sourceauth-syntax.json"></a>

```
{
  "[Type](#cfn-codebuild-project-sourceauth-type)" : String,
  "[Resource](#cfn-codebuild-project-sourceauth-resource)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-sourceauth-syntax.yaml"></a>

```
[Type](#cfn-codebuild-project-sourceauth-type): String
[Resource](#cfn-codebuild-project-sourceauth-resource): String
```

## Properties<a name="aws-properties-codebuild-project-sourceauth-properties"></a>

`Type`  <a name="cfn-codebuild-project-sourceauth-type"></a>
The authorization type to use\. The only valid value is `OAUTH`, which represents the OAuth authorization type\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Resource`  <a name="cfn-codebuild-project-sourceauth-resource"></a>
The resource value that applies to the specified authorization type\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 