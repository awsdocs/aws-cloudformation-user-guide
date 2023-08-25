# AWS::EntityResolution::MatchingWorkflow<a name="aws-resource-entityresolution-matchingworkflow"></a>

Creates a `MatchingWorkflow` object which stores the configuration of the data processing job to be run\. It is important to note that there should not be a pre\-existing `MatchingWorkflow` with the same name\. To modify an existing workflow, utilize the `UpdateMatchingWorkflow` API\.

## Syntax<a name="aws-resource-entityresolution-matchingworkflow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-entityresolution-matchingworkflow-syntax.json"></a>

```
{
  "Type" : "AWS::EntityResolution::MatchingWorkflow",
  "Properties" : {
      "[Description](#cfn-entityresolution-matchingworkflow-description)" : String,
      "[InputSourceConfig](#cfn-entityresolution-matchingworkflow-inputsourceconfig)" : [ InputSource, ... ],
      "[OutputSourceConfig](#cfn-entityresolution-matchingworkflow-outputsourceconfig)" : [ OutputSource, ... ],
      "[ResolutionTechniques](#cfn-entityresolution-matchingworkflow-resolutiontechniques)" : ResolutionTechniques,
      "[RoleArn](#cfn-entityresolution-matchingworkflow-rolearn)" : String,
      "[Tags](#cfn-entityresolution-matchingworkflow-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WorkflowName](#cfn-entityresolution-matchingworkflow-workflowname)" : String
    }
}
```

### YAML<a name="aws-resource-entityresolution-matchingworkflow-syntax.yaml"></a>

```
Type: AWS::EntityResolution::MatchingWorkflow
Properties: 
  [Description](#cfn-entityresolution-matchingworkflow-description): String
  [InputSourceConfig](#cfn-entityresolution-matchingworkflow-inputsourceconfig): 
    - InputSource
  [OutputSourceConfig](#cfn-entityresolution-matchingworkflow-outputsourceconfig): 
    - OutputSource
  [ResolutionTechniques](#cfn-entityresolution-matchingworkflow-resolutiontechniques): 
    ResolutionTechniques
  [RoleArn](#cfn-entityresolution-matchingworkflow-rolearn): String
  [Tags](#cfn-entityresolution-matchingworkflow-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WorkflowName](#cfn-entityresolution-matchingworkflow-workflowname): String
```

## Properties<a name="aws-resource-entityresolution-matchingworkflow-properties"></a>

`Description`  <a name="cfn-entityresolution-matchingworkflow-description"></a>
A description of the workflow\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputSourceConfig`  <a name="cfn-entityresolution-matchingworkflow-inputsourceconfig"></a>
A list of `InputSource` objects, which have the fields `InputSourceARN` and `SchemaName`\.  
*Required*: Yes  
*Type*: List of [InputSource](aws-properties-entityresolution-matchingworkflow-inputsource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputSourceConfig`  <a name="cfn-entityresolution-matchingworkflow-outputsourceconfig"></a>
A list of `OutputSource` objects, each of which contains fields `OutputS3Path`, `ApplyNormalization`, and `Output`\.  
*Required*: Yes  
*Type*: List of [OutputSource](aws-properties-entityresolution-matchingworkflow-outputsource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResolutionTechniques`  <a name="cfn-entityresolution-matchingworkflow-resolutiontechniques"></a>
An object which defines the `resolutionType` and the `ruleBasedProperties`  
*Required*: Yes  
*Type*: [ResolutionTechniques](aws-properties-entityresolution-matchingworkflow-resolutiontechniques.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-entityresolution-matchingworkflow-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role\. Entity Resolution assumes this role to create resources on your behalf as part of workflow execution\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-entityresolution-matchingworkflow-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkflowName`  <a name="cfn-entityresolution-matchingworkflow-workflowname"></a>
The name of the workflow\. There cannot be multiple `DataIntegrationWorkflows` with the same name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)