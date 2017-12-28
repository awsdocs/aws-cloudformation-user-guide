# AWS CodePipeline Pipeline Stages Actions<a name="aws-properties-codepipeline-pipeline-stages-actions"></a>

`Actions` is a property of the [AWS CodePipeline Pipeline Stages](aws-properties-codepipeline-pipeline-stages.md) property that specifies an action for an AWS CodePipeline stage\.

## Syntax<a name="w3ab2c21c14d390b5"></a>

### JSON<a name="aws-properties-codepipeline-pipeline-stages-actions-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid)" : ActionTypeID,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-configuration)" : { Key : Value },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-inputartifacts)" : [ InputArtifacts, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-outputartifacts)" : [ OutputArtifacts, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-rolearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-runorder)" : Integer
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-actions-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-actiontypeid):
  ActionTypeID
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-configuration):
  Key : Value
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-inputartifacts):
  - InputArtifacts
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-outputartifacts):
  - OutputArtifacts
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-rolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-pipeline-stages-actions-runorder): Integer
```

## Properties<a name="w3ab2c21c14d390b7"></a>

`ActionTypeId`  
Specifies the action type and the provider of the action\.  
*Required: *Yes  
*Type*: [AWS CodePipeline Pipeline Stages Actions ActionTypeId](aws-properties-codepipeline-pipeline-stages-actions-actiontypeid.md)

`Configuration`  
The action's configuration\. These are key\-value pairs that specify input values for an action\. For more information, see [ Action Structure Requirements in AWS CodePipeline](http://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html#action-requirements) in the *AWS CodePipeline User Guide*\.  
*Required: *No  
*Type*: JSON object

`InputArtifacts`  
The name or ID of the artifact that the action consumes, such as a test or build artifact\.  
*Required: *No  
*Type*: List of [AWS CodePipeline Pipeline Stages Actions InputArtifacts](aws-properties-codepipeline-pipeline-stages-actions-inputartifacts.md)

`Name`  
The action name\.  
*Required: *Yes  
*Type*: String

`OutputArtifacts`  
The artifact name or ID that is a result of the action, such as a test or build artifact\.  
*Required: *No  
*Type*: List of [AWS CodePipeline Pipeline Stages Actions OutputArtifacts](aws-properties-codepipeline-pipeline-stages-actions-outputartifacts.md)

`RoleArn`  
The Amazon Resource Name \(ARN\) of a service role that the action uses\. The pipeline's role assumes this role\.  
*Required: *No  
*Type*: String

`RunOrder`  
The order in which AWS CodePipeline runs this action\.  
*Required: *No  
*Type*: Integer