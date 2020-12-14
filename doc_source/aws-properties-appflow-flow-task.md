# AWS::AppFlow::Flow Task<a name="aws-properties-appflow-flow-task"></a>

 The `Task` property type specifies the class for modeling different type of tasks\. Task implementation varies based on the `TaskType`\. 

## Syntax<a name="aws-properties-appflow-flow-task-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-task-syntax.json"></a>

```
{
  "[ConnectorOperator](#cfn-appflow-flow-task-connectoroperator)" : ConnectorOperator,
  "[DestinationField](#cfn-appflow-flow-task-destinationfield)" : String,
  "[SourceFields](#cfn-appflow-flow-task-sourcefields)" : [ String, ... ],
  "[TaskProperties](#cfn-appflow-flow-task-taskproperties)" : [ TaskPropertiesObject, ... ],
  "[TaskType](#cfn-appflow-flow-task-tasktype)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-task-syntax.yaml"></a>

```
  [ConnectorOperator](#cfn-appflow-flow-task-connectoroperator): 
    ConnectorOperator
  [DestinationField](#cfn-appflow-flow-task-destinationfield): String
  [SourceFields](#cfn-appflow-flow-task-sourcefields): 
    - String
  [TaskProperties](#cfn-appflow-flow-task-taskproperties): 
    - TaskPropertiesObject
  [TaskType](#cfn-appflow-flow-task-tasktype): String
```

## Properties<a name="aws-properties-appflow-flow-task-properties"></a>

`ConnectorOperator`  <a name="cfn-appflow-flow-task-connectoroperator"></a>
 The operation to be performed on the provided source fields\.   
*Required*: No  
*Type*: [ConnectorOperator](aws-properties-appflow-flow-connectoroperator.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationField`  <a name="cfn-appflow-flow-task-destinationfield"></a>
 A field in a destination connector, or a field value against which Amazon AppFlow validates a source field\.   
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFields`  <a name="cfn-appflow-flow-task-sourcefields"></a>
 The source fields to which a particular task is applied\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskProperties`  <a name="cfn-appflow-flow-task-taskproperties"></a>
 A map used to store task\-related information\. The execution service looks for particular information based on the `TaskType`\.   
*Required*: No  
*Type*: List of [TaskPropertiesObject](aws-properties-appflow-flow-taskpropertiesobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskType`  <a name="cfn-appflow-flow-task-tasktype"></a>
 Specifies the particular task implementation that Amazon AppFlow performs\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `Arithmetic | Filter | Map | Mask | Merge | Truncate | Validate`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-task--seealso"></a>
+ [Task](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_Task.html) in the *Amazon AppFlow API Reference*\.

