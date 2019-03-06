# CodePipeline Pipeline Stages Blockers<a name="aws-properties-codepipeline-pipeline-stages-blockers"></a>

`Blockers` is a property of the [CodePipeline Pipeline Stages](aws-properties-codepipeline-pipeline-stages.md) property that specifies an CodePipeline gate declaration\.

## Syntax<a name="w13ab1c21c10c81c17c33b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-blockers-syntax.json"></a>

```
{
  "[Name](#cfn-codepipeline-pipeline-stages-blockers-name)" : String,
  "[Type](#cfn-codepipeline-pipeline-stages-blockers-type)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-blockers-syntax.yaml"></a>

```
[Name](#cfn-codepipeline-pipeline-stages-blockers-name): String
[Type](#cfn-codepipeline-pipeline-stages-blockers-type): String
```

## Properties<a name="w13ab1c21c10c81c17c33b7"></a>

`Name`  <a name="cfn-codepipeline-pipeline-stages-blockers-name"></a>
The name of the gate declaration\.  
*Required*: Yes  
*Type*: String

`Type`  <a name="cfn-codepipeline-pipeline-stages-blockers-type"></a>
The type of gate declaration\. For valid values, see [BlockerDeclaration](https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_BlockerDeclaration.html) in the *AWS CodePipeline API Reference*\.  
*Required*: Yes  
*Type*: String