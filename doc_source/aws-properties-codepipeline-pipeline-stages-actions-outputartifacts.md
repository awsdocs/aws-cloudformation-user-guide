# CodePipeline Pipeline Stages Actions OutputArtifacts<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts"></a>

`OutputArtifacts` is a property of the [CodePipeline Pipeline Stages Actions](aws-properties-codepipeline-pipeline-stages-actions.md) property that specifies an artifact that is the result of an CodePipeline action, such as a test or build artifact\.

## Syntax<a name="w13ab1c21c10c81c17c49b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts-syntax.json"></a>

```
{
  "[Name](#cfn-codepipeline-pipeline-stages-actions-outputartifacts-name)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts-syntax.yaml"></a>

```
[Name](#cfn-codepipeline-pipeline-stages-actions-outputartifacts-name): String
```

## Properties<a name="w13ab1c21c10c81c17c49b7"></a>

`Name`  <a name="cfn-codepipeline-pipeline-stages-actions-outputartifacts-name"></a>
The name of the artifact that is the result of an CodePipeline action, such as `My App`\. Output artifact names must be unique within a pipeline\.  
*Required*: Yes  
*Type*: String