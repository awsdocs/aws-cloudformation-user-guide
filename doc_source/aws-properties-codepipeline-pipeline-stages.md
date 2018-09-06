# AWS CodePipeline Pipeline Stages<a name="aws-properties-codepipeline-pipeline-stages"></a>

`Stages` is a property of the [AWS::CodePipeline::Pipeline](aws-resource-codepipeline-pipeline.md) resource that specifies a sequence of tasks for AWS CodePipeline to complete on an artifact\.

## Syntax<a name="w3ab2c21c14d460b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-syntax.json"></a>

```
{
  "[Actions](#cfn-codepipeline-pipeline-stages-actions)" : [ Actions, ... ],
  "[Blockers](#cfn-codepipeline-pipeline-stages-blockers)" : [ Blockers, ... ],
  "[Name](#cfn-codepipeline-pipeline-stages-name)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-syntax.yaml"></a>

```
[Actions](#cfn-codepipeline-pipeline-stages-actions):
  - Actions
[Blockers](#cfn-codepipeline-pipeline-stages-blockers):
  - Blockers
[Name](#cfn-codepipeline-pipeline-stages-name): String
```

## Properties<a name="w3ab2c21c14d460b7"></a>

`Actions`  <a name="cfn-codepipeline-pipeline-stages-actions"></a>
The actions to include in this stage\.  
*Required*: Yes  
*Type*: List of [AWS CodePipeline Pipeline Stages Actions](aws-properties-codepipeline-pipeline-stages-actions.md)

`Blockers`  <a name="cfn-codepipeline-pipeline-stages-blockers"></a>
The gates included in a stage\.  
*Required*: No  
*Type*: List of [AWS CodePipeline Pipeline Stages Blockers](aws-properties-codepipeline-pipeline-stages-blockers.md)

`Name`  <a name="cfn-codepipeline-pipeline-stages-name"></a>
A name for this stage\.  
*Required*: Yes  
*Type*: String