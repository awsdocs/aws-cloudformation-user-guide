# AWS::CustomerProfiles::Integration Task<a name="aws-properties-customerprofiles-integration-task"></a>

The `Task` property type specifies the class for modeling different type of tasks\. Task implementation varies based on the TaskType\.

## Syntax<a name="aws-properties-customerprofiles-integration-task-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-task-syntax.json"></a>

```
{
  "[ConnectorOperator](#cfn-customerprofiles-integration-task-connectoroperator)" : ConnectorOperator,
  "[DestinationField](#cfn-customerprofiles-integration-task-destinationfield)" : String,
  "[SourceFields](#cfn-customerprofiles-integration-task-sourcefields)" : [ String, ... ],
  "[TaskProperties](#cfn-customerprofiles-integration-task-taskproperties)" : [ TaskPropertiesMap, ... ],
  "[TaskType](#cfn-customerprofiles-integration-task-tasktype)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-integration-task-syntax.yaml"></a>

```
  [ConnectorOperator](#cfn-customerprofiles-integration-task-connectoroperator): 
    ConnectorOperator
  [DestinationField](#cfn-customerprofiles-integration-task-destinationfield): String
  [SourceFields](#cfn-customerprofiles-integration-task-sourcefields): 
    - String
  [TaskProperties](#cfn-customerprofiles-integration-task-taskproperties): 
    - TaskPropertiesMap
  [TaskType](#cfn-customerprofiles-integration-task-tasktype): String
```

## Properties<a name="aws-properties-customerprofiles-integration-task-properties"></a>

`ConnectorOperator`  <a name="cfn-customerprofiles-integration-task-connectoroperator"></a>
The operation to be performed on the provided source fields\.  
*Required*: No  
*Type*: [ConnectorOperator](aws-properties-customerprofiles-integration-connectoroperator.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationField`  <a name="cfn-customerprofiles-integration-task-destinationfield"></a>
A field in a destination connector, or a field value against which Amazon AppFlow validates a source field\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFields`  <a name="cfn-customerprofiles-integration-task-sourcefields"></a>
The source fields to which a particular task is applied\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskProperties`  <a name="cfn-customerprofiles-integration-task-taskproperties"></a>
A map used to store task\-related information\. The service looks for particular information based on the TaskType\.  
*Required*: No  
*Type*: List of [TaskPropertiesMap](aws-properties-customerprofiles-integration-taskpropertiesmap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskType`  <a name="cfn-customerprofiles-integration-task-tasktype"></a>
Specifies the particular task implementation that Amazon AppFlow performs\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Arithmetic | Filter | Map | Mask | Merge | Truncate | Validate`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)