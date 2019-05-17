# AWS::CodePipeline::CustomActionType ArtifactDetails<a name="aws-properties-codepipeline-customactiontype-artifactdetails"></a>

Returns information about the details of an artifact\.

## Syntax<a name="aws-properties-codepipeline-customactiontype-artifactdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-customactiontype-artifactdetails-syntax.json"></a>

```
{
  "[MaximumCount](#cfn-codepipeline-customactiontype-artifactdetails-maximumcount)" : Integer,
  "[MinimumCount](#cfn-codepipeline-customactiontype-artifactdetails-minimumcount)" : Integer
}
```

### YAML<a name="aws-properties-codepipeline-customactiontype-artifactdetails-syntax.yaml"></a>

```
  [MaximumCount](#cfn-codepipeline-customactiontype-artifactdetails-maximumcount): Integer
  [MinimumCount](#cfn-codepipeline-customactiontype-artifactdetails-minimumcount): Integer
```

## Properties<a name="aws-properties-codepipeline-customactiontype-artifactdetails-properties"></a>

`MaximumCount`  <a name="cfn-codepipeline-customactiontype-artifactdetails-maximumcount"></a>
The maximum number of artifacts allowed for the action type\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumCount`  <a name="cfn-codepipeline-customactiontype-artifactdetails-minimumcount"></a>
The minimum number of artifacts allowed for the action type\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)