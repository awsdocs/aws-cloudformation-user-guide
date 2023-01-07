# AWS::CodePipeline::Pipeline StageTransition<a name="aws-properties-codepipeline-pipeline-disableinboundstagetransitions"></a>

The name of the pipeline in which you want to disable the flow of artifacts from one stage to another\.

## Syntax<a name="aws-properties-codepipeline-pipeline-disableinboundstagetransitions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-pipeline-disableinboundstagetransitions-syntax.json"></a>

```
{
  "[Reason](#cfn-codepipeline-pipeline-disableinboundstagetransitions-reason)" : String,
  "[StageName](#cfn-codepipeline-pipeline-disableinboundstagetransitions-stagename)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-disableinboundstagetransitions-syntax.yaml"></a>

```
  [Reason](#cfn-codepipeline-pipeline-disableinboundstagetransitions-reason): String
  [StageName](#cfn-codepipeline-pipeline-disableinboundstagetransitions-stagename): String
```

## Properties<a name="aws-properties-codepipeline-pipeline-disableinboundstagetransitions-properties"></a>

`Reason`  <a name="cfn-codepipeline-pipeline-disableinboundstagetransitions-reason"></a>
The reason given to the user that a stage is disabled, such as waiting for manual approval or manual tests\. This message is displayed in the pipeline console UI\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `300`  
*Pattern*: `[a-zA-Z0-9!@ \(\)\.\*\?\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StageName`  <a name="cfn-codepipeline-pipeline-disableinboundstagetransitions-stagename"></a>
The name of the stage where you want to disable the inbound or outbound transition of artifacts\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[A-Za-z0-9.@\-_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)