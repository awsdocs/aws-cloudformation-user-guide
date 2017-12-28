# AWS CodePipeline CustomActionType ArtifactDetails<a name="aws-resource-codepipeline-customactiontype-artifactdetails"></a>

`ArtifactDetails` is a property of the [AWS::CodePipeline::CustomActionType](aws-resource-codepipeline-customactiontype.md) resource that specifies the details of an artifact for an AWS CodePipeline custom action\. For valid values, see [ArtifactDetails](http://docs.aws.amazon.com/codepipeline/latest/APIReference/API_ArtifactDetails.html) in the *AWS CodePipeline API Reference*\.

## Syntax<a name="w3ab2c21c14d362b5"></a>

### JSON<a name="aws-properties-codepipeline-customactiontype-artifactdetails-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-artifactdetails-maximumcount)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-artifactdetails-minimumcount)" : Integer
}
```

### Yaml<a name="aws-properties-codepipeline-customactiontype-artifactdetails-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-artifactdetails-maximumcount): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-artifactdetails-minimumcount): Integer
```

## Properties<a name="w3ab2c21c14d362b7"></a>

`MaximumCount`  
The maximum number of artifacts allowed for the action type\.  
*Required: *Yes  
*Type*: Integer

`MinimumCount`  
The minimum number of artifacts allowed for the action type\.  
*Required: *Yes  
*Type*: Integer