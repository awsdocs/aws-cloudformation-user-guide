# AWS::CodeBuild::Project SourceAuth<a name="aws-properties-codebuild-project-sourceauth"></a>

 `SourceAuth` is a property of the [AWS CodeBuild Project Source ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-source.html) property type that specifies authorization settings for AWS CodeBuild to access the source code to be built\. 

 `SourceAuth` is for use by the CodeBuild console only\. Do not get or set it directly\. 

## Syntax<a name="aws-properties-codebuild-project-sourceauth-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-sourceauth-syntax.json"></a>

```
{
  "[Resource](#cfn-codebuild-project-sourceauth-resource)" : String,
  "[Type](#cfn-codebuild-project-sourceauth-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-sourceauth-syntax.yaml"></a>

```
  [Resource](#cfn-codebuild-project-sourceauth-resource): String
  [Type](#cfn-codebuild-project-sourceauth-type): String
```

## Properties<a name="aws-properties-codebuild-project-sourceauth-properties"></a>

`Resource`  <a name="cfn-codebuild-project-sourceauth-resource"></a>
 The resource value that applies to the specified authorization type\.   
 This data type is used by the AWS CodeBuild console only\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codebuild-project-sourceauth-type"></a>
The authorization type to use\. The only valid value is `OAUTH`, which represents the OAuth authorization type\.  
 This data type is used by the AWS CodeBuild console only\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `OAUTH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)