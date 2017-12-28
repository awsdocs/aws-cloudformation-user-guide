# AWS CodePipeline Pipeline Stages<a name="aws-properties-codepipeline-pipeline-stages"></a>

`Stages` is a property of the [AWS::CodePipeline::Pipeline](aws-resource-codepipeline-pipeline.md) resource that specifies a sequence of tasks for AWS CodePipeline to complete on an artifact\.

## Syntax<a name="w3ab2c21c14d386b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions)" : [ Actions, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-blockers)" : [ Blockers, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-name)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions):
  - Actions
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-blockers):
  - Blockers
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-name): String
```

## Properties<a name="w3ab2c21c14d386b7"></a>

`Actions`  
The actions to include in this stage\.  
*Required: *Yes  
*Type*: List of [AWS CodePipeline Pipeline Stages Actions](aws-properties-codepipeline-pipeline-stages-actions.md)

`Blockers`  
The gates included in a stage\.  
*Required: *No  
*Type*: List of [AWS CodePipeline Pipeline Stages Blockers](aws-properties-codepipeline-pipeline-stages-blockers.md)

`Name`  
A name for this stage\.  
*Required: *Yes  
*Type*: String