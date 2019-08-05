# AWS::CodePipeline::Pipeline ArtifactStoreMap<a name="aws-properties-codepipeline-pipeline-artifactstoremap"></a>

A mapping of `artifactStore` objects and their corresponding regions\. There must be an artifact store for the pipeline region and for each cross\-region action within the pipeline\. You can only use either `artifactStore` or `artifactStores`, not both\.

If you create a cross\-region action in your pipeline, you must use `artifactStores`\.

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
Represents information about the Amazon S3 bucket where artifacts are stored for the pipeline\.
*Required*: Yes
*Type*: [ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-codepipeline-pipeline-artifactstoremap-region"></a>
The action declaration's AWS Region, such as us\-east\-1\.
*Required*: Yes
*Type*: String
*Minimum*: `4`
*Maximum*: `30`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
