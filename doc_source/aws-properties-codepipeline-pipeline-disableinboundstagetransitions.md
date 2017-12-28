# AWS CodePipeline Pipeline DisableInboundStageTransitions<a name="aws-properties-codepipeline-pipeline-disableinboundstagetransitions"></a>

`DisableInboundStageTransitions` is a property of the [AWS::CodePipeline::Pipeline](aws-resource-codepipeline-pipeline.md) resource that specifies which AWS CodePipeline stage to disable transitions to\.

## Syntax<a name="w3ab2c21c14d382b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-disableinboundstagetransitions-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-disableinboundstagetransitions-reason)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-disableinboundstagetransitions-stagename)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-disableinboundstagetransitions-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-disableinboundstagetransitions-reason): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-disableinboundstagetransitions-stagename): String
```

## Properties<a name="w3ab2c21c14d382b7"></a>

`Reason`  
An explanation of why the transition between two stages of a pipeline was disabled\.  
*Required: *Yes  
*Type*: String

`StageName`  
The name of the stage to which transitions are disabled\.  
*Required: *Yes  
*Type*: String