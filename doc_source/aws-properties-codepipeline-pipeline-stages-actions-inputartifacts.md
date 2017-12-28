# AWS CodePipeline Pipeline Stages Actions InputArtifacts<a name="aws-properties-codepipeline-pipeline-stages-actions-inputartifacts"></a>

`InputArtifacts` is a property of the [AWS CodePipeline Pipeline Stages Actions](aws-properties-codepipeline-pipeline-stages-actions.md) property that specifies an artifact that the AWS CodePipeline action works on, such as a test or build artifact\.

## Syntax<a name="w3ab2c21c14d398b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-actions-inputartifacts-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-inputartifacts-name)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-actions-inputartifacts-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-inputartifacts-name): String
```

## Properties<a name="w3ab2c21c14d398b7"></a>

`Name`  
The name of the artifact that the AWS CodePipeline action works on, such as `My App`\.The input artifact of an action must match the output artifact from any preceding action\.  
*Required: *Yes  
*Type*: String