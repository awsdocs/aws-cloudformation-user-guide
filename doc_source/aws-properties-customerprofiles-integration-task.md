# AWS::CustomerProfiles::Integration Task<a name="aws-properties-customerprofiles-integration-task"></a>

<a name="aws-properties-customerprofiles-integration-task-description"></a>The `Task` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::CustomerProfiles::Integration](aws-resource-customerprofiles-integration.md)\.

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
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [ConnectorOperator](aws-properties-customerprofiles-integration-connectoroperator.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationField`  <a name="cfn-customerprofiles-integration-task-destinationfield"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFields`  <a name="cfn-customerprofiles-integration-task-sourcefields"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskProperties`  <a name="cfn-customerprofiles-integration-task-taskproperties"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [TaskPropertiesMap](aws-properties-customerprofiles-integration-taskpropertiesmap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskType`  <a name="cfn-customerprofiles-integration-task-tasktype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)