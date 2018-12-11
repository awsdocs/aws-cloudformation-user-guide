# AWS CodePipeline Pipeline ArtifactStoreMap<a name="aws-properties-codepipeline-pipeline-artifactstoremap"></a>

<a name="aws-properties-codepipeline-pipeline-artifactstoremap-description"></a>The `ArtifactStoreMap` property type specifies a mapping of an ArtifactStore object and its corresponding region\.

<a name="aws-properties-codepipeline-pipeline-artifactstoremap-inheritance"></a> `ArtifactStoreMap` is a property of the [AWS::CodePipeline::Pipeline](aws-resource-codepipeline-pipeline.md) resource type\.

## Syntax<a name="aws-properties-codepipeline-pipeline-artifactstoremap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-pipeline-artifactstoremap-syntax.json"></a>

```
{
  "[ArtifactStore](#cfn-codepipeline-pipeline-artifactstoremap-artifactstore)" : [ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md),
  "[Region](#cfn-codepipeline-pipeline-artifactstoremap-region)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-artifactstoremap-syntax.yaml"></a>

```
[ArtifactStore](#cfn-codepipeline-pipeline-artifactstoremap-artifactstore): 
    [ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md)
[Region](#cfn-codepipeline-pipeline-artifactstoremap-region): String
```

## Properties<a name="aws-properties-codepipeline-pipeline-artifactstoremap-properties"></a>

`ArtifactStore`  <a name="cfn-codepipeline-pipeline-artifactstoremap-artifactstore"></a>
The Amazon S3 bucket where artifacts are stored for the pipeline\.  
*Required*: Yes  
*Type*: [ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Region`  <a name="cfn-codepipeline-pipeline-artifactstoremap-region"></a>
Specifies the action’s AWS Region, such as `us-east-1`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)