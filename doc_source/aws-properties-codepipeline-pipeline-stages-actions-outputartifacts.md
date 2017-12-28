# AWS CodePipeline Pipeline Stages Actions OutputArtifacts<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts"></a>

`OutputArtifacts` is a property of the [AWS CodePipeline Pipeline Stages Actions](aws-properties-codepipeline-pipeline-stages-actions.md) property that specifies an artifact that is the result of an AWS CodePipeline action, such as a test or build artifact\.

## Syntax<a name="w3ab2c21c14d402b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-outputartifacts-name)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-outputartifacts-name): String
```

## Properties<a name="w3ab2c21c14d402b7"></a>

`Name`  
The name of the artifact that is the result of an AWS CodePipeline action, such as `My App`\. Output artifact names must be unique within a pipeline\.  
*Required: *Yes  
*Type*: String