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
*Allowed Values*: `OAUTH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-east-1`
- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `cn-northwest-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `me-south-1`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
