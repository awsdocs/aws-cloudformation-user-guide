# AWS::CodePipeline::Pipeline ActionDeclaration<a name="aws-properties-codepipeline-pipeline-stages-actions"></a>

Represents information about an action declaration\.

## Syntax<a name="aws-properties-codepipeline-pipeline-stages-actions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-pipeline-stages-actions-syntax.json"></a>

```
{
  "[ActionTypeId](#cfn-codepipeline-pipeline-stages-actions-actiontypeid)" : ActionTypeId,
  "[Configuration](#cfn-codepipeline-pipeline-stages-actions-configuration)" : Json,
  "[InputArtifacts](#cfn-codepipeline-pipeline-stages-actions-inputartifacts)" : [ InputArtifact, ... ],
  "[Name](#cfn-codepipeline-pipeline-stages-actions-name)" : String,
  "[Namespace](#cfn-codepipeline-pipeline-actiondeclaration-namespace)" : String,
  "[OutputArtifacts](#cfn-codepipeline-pipeline-stages-actions-outputartifacts)" : [ OutputArtifact, ... ],
  "[Region](#cfn-codepipeline-pipeline-stages-actions-region)" : String,
  "[RoleArn](#cfn-codepipeline-pipeline-stages-actions-rolearn)" : String,
  "[RunOrder](#cfn-codepipeline-pipeline-stages-actions-runorder)" : Integer
}
```

### YAML<a name="aws-properties-codepipeline-pipeline-stages-actions-syntax.yaml"></a>

```
  [ActionTypeId](#cfn-codepipeline-pipeline-stages-actions-actiontypeid): 
    ActionTypeId
  [Configuration](#cfn-codepipeline-pipeline-stages-actions-configuration): Json
  [InputArtifacts](#cfn-codepipeline-pipeline-stages-actions-inputartifacts): 
    - InputArtifact
  [Name](#cfn-codepipeline-pipeline-stages-actions-name): String
  [Namespace](#cfn-codepipeline-pipeline-actiondeclaration-namespace): String
  [OutputArtifacts](#cfn-codepipeline-pipeline-stages-actions-outputartifacts): 
    - OutputArtifact
  [Region](#cfn-codepipeline-pipeline-stages-actions-region): String
  [RoleArn](#cfn-codepipeline-pipeline-stages-actions-rolearn): String
  [RunOrder](#cfn-codepipeline-pipeline-stages-actions-runorder): Integer
```

## Properties<a name="aws-properties-codepipeline-pipeline-stages-actions-properties"></a>

`ActionTypeId`  <a name="cfn-codepipeline-pipeline-stages-actions-actiontypeid"></a>
Specifies the action type and the provider of the action\.  
*Required*: Yes  
*Type*: [ActionTypeId](aws-properties-codepipeline-pipeline-stages-actions-actiontypeid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Configuration`  <a name="cfn-codepipeline-pipeline-stages-actions-configuration"></a>
The action's configuration\. These are key\-value pairs that specify input values for an action\. For more information, see [Action Structure Requirements in CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html#action-requirements)\. For the list of configuration properties for the AWS CloudFormation action type in CodePipeline, see [Configuration Properties Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline-action-reference.html) in the *AWS CloudFormation User Guide*\. For template snippets with examples, see [Using Parameter Override Functions with CodePipeline Pipelines](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline-parameter-override-functions.html) in the *AWS CloudFormation User Guide*\.  
The values can be represented in either JSON or YAML format\. For example, the JSON configuration item format is as follows:   
 *JSON:*   
 `"Configuration" : { Key : Value },`   
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputArtifacts`  <a name="cfn-codepipeline-pipeline-stages-actions-inputartifacts"></a>
The name or ID of the artifact consumed by the action, such as a test or build artifact\.  
For a CodeBuild action with multiple input artifacts, one of your input sources must be designated the PrimarySource\. For more information, see the [CodeBuild action reference page](https://docs.aws.amazon.com/codepipeline/latest/userguide/action-reference-CodeBuild.html) in the *AWS CodePipeline User Guide*\.
*Required*: No  
*Type*: List of [InputArtifact](aws-properties-codepipeline-pipeline-stages-actions-inputartifacts.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-codepipeline-pipeline-stages-actions-name"></a>
The action declaration's name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[A-Za-z0-9.@\-_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Namespace`  <a name="cfn-codepipeline-pipeline-actiondeclaration-namespace"></a>
The variable namespace associated with the action\. All variables produced as output by this action fall under this namespace\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[A-Za-z0-9@\-_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputArtifacts`  <a name="cfn-codepipeline-pipeline-stages-actions-outputartifacts"></a>
The name or ID of the result of the action declaration, such as a test or build artifact\.  
*Required*: No  
*Type*: List of [OutputArtifact](aws-properties-codepipeline-pipeline-stages-actions-outputartifacts.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-codepipeline-pipeline-stages-actions-region"></a>
The action declaration's AWS Region, such as us\-east\-1\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-codepipeline-pipeline-stages-actions-rolearn"></a>
The ARN of the IAM service role that performs the declared action\. This is assumed through the roleArn for the pipeline\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `arn:aws(-[\w]+)*:iam::[0-9]{12}:role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunOrder`  <a name="cfn-codepipeline-pipeline-stages-actions-runorder"></a>
The order in which actions are run\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `999`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)