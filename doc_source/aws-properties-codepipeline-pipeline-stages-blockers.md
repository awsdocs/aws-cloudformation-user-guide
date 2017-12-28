# AWS CodePipeline Pipeline Stages Blockers<a name="aws-properties-codepipeline-pipeline-stages-blockers"></a>

`Blockers` is a property of the [AWS CodePipeline Pipeline Stages](aws-properties-codepipeline-pipeline-stages.md) property that specifies an AWS CodePipeline gate declaration\.

## Syntax<a name="w3ab2c21c14d406b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-blockers-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-blockers-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-blockers-type)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-blockers-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-blockers-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-blockers-type): String
```

## Properties<a name="w3ab2c21c14d406b7"></a>

`Name`  
The name of the gate declaration\.  
*Required: *Yes  
*Type*: String

`Type`  
The type of gate declaration\. For valid values, see [BlockerDeclaration](http://docs.aws.amazon.com/codepipeline/latest/APIReference/API_BlockerDeclaration.html) in the *AWS CodePipeline API Reference*\.  
*Required: *Yes  
*Type*: String