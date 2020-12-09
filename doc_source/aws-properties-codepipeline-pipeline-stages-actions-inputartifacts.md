# AWS::CodePipeline::Pipeline InputArtifact<a name="aws-properties-codepipeline-pipeline-stages-actions-inputartifacts"></a>

Represents information about an artifact to be worked on, such as a test or build artifact\.

## Syntax<a name="aws-properties-codepipeline-pipeline-stages-actions-inputartifacts-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-pipeline-stages-actions-inputartifacts-syntax.json"></a>

```
{
  "[Name](#cfn-codepipeline-pipeline-stages-actions-inputartifacts-name)" : String
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-actions-inputartifacts-syntax.yaml"></a>

```
  [Name](#cfn-codepipeline-pipeline-stages-actions-inputartifacts-name): String
```

## Properties<a name="aws-properties-codepipeline-pipeline-stages-actions-inputartifacts-properties"></a>

`Name`  <a name="cfn-codepipeline-pipeline-stages-actions-inputartifacts-name"></a>
The name of the artifact to be worked on \(for example, "My App"\)\.  
The input artifact of an action must exactly match the output artifact declared in a preceding action, but the input artifact does not have to be the next action in strict sequence from the action that provided the output artifact\. Actions in parallel can declare different output artifacts, which are in turn consumed by different following actions\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[a-zA-Z0-9_\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)