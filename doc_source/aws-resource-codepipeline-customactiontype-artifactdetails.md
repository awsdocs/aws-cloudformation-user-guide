# AWS CodePipeline CustomActionType ArtifactDetails<a name="aws-resource-codepipeline-customactiontype-artifactdetails"></a>

`ArtifactDetails` is a property of the [AWS::CodePipeline::CustomActionType](aws-resource-codepipeline-customactiontype.md) resource that specifies the details of an artifact for an AWS CodePipeline custom action\. For valid values, see [ArtifactDetails](https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_ArtifactDetails.html) in the *AWS CodePipeline API Reference*\.

## Syntax<a name="w4ab1c21c10c75c13c17b5"></a>

### JSON<a name="aws-properties-codepipeline-customactiontype-artifactdetails-syntax.json"></a>

```
{
  "[MaximumCount](#cfn-codepipeline-customactiontype-artifactdetails-maximumcount)" : Integer,
  "[MinimumCount](#cfn-codepipeline-customactiontype-artifactdetails-minimumcount)" : Integer
}
```

### Yaml<a name="aws-properties-codepipeline-customactiontype-artifactdetails-syntax.yaml"></a>

```
[MaximumCount](#cfn-codepipeline-customactiontype-artifactdetails-maximumcount): Integer
[MinimumCount](#cfn-codepipeline-customactiontype-artifactdetails-minimumcount): Integer
```

## Properties<a name="w4ab1c21c10c75c13c17b7"></a>

`MaximumCount`  <a name="cfn-codepipeline-customactiontype-artifactdetails-maximumcount"></a>
The maximum number of artifacts allowed for the action type\.  
*Required*: Yes  
*Type*: Integer

`MinimumCount`  <a name="cfn-codepipeline-customactiontype-artifactdetails-minimumcount"></a>
The minimum number of artifacts allowed for the action type\.  
*Required*: Yes  
*Type*: Integer