# AWS::CodePipeline::Pipeline OutputArtifact<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts"></a>

Represents information about the output of an action\.

## Syntax<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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

## Properties<a name="aws-properties-codepipeline-pipeline-stages-actions-outputartifacts-properties"></a>

`Name`  <a name="cfn-codepipeline-pipeline-stages-actions-outputartifacts-name"></a>
The name of the output of an artifact, such as "My App"\.  
The output artifact name must exactly match the input artifact declared for a downstream action\. However, the downstream action's input artifact does not have to be the next action in strict sequence from the action that provided the output artifact\. Actions in parallel can declare different output artifacts, which are in turn consumed by different following actions\.  
Output artifact names must be unique within a pipeline\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[a-zA-Z0-9_\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)