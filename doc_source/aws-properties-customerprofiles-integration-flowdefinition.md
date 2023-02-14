# AWS::CustomerProfiles::Integration FlowDefinition<a name="aws-properties-customerprofiles-integration-flowdefinition"></a>

<a name="aws-properties-customerprofiles-integration-flowdefinition-description"></a>The `FlowDefinition` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::CustomerProfiles::Integration](aws-resource-customerprofiles-integration.md)\.

## Syntax<a name="aws-properties-customerprofiles-integration-flowdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-flowdefinition-syntax.json"></a>

```
{
  "[Description](#cfn-customerprofiles-integration-flowdefinition-description)" : String,
  "[FlowName](#cfn-customerprofiles-integration-flowdefinition-flowname)" : String,
  "[KmsArn](#cfn-customerprofiles-integration-flowdefinition-kmsarn)" : String,
  "[SourceFlowConfig](#cfn-customerprofiles-integration-flowdefinition-sourceflowconfig)" : SourceFlowConfig,
  "[Tasks](#cfn-customerprofiles-integration-flowdefinition-tasks)" : [ Task, ... ],
  "[TriggerConfig](#cfn-customerprofiles-integration-flowdefinition-triggerconfig)" : TriggerConfig
}
```

### YAML<a name="aws-properties-customerprofiles-integration-flowdefinition-syntax.yaml"></a>

```
  [Description](#cfn-customerprofiles-integration-flowdefinition-description): String
  [FlowName](#cfn-customerprofiles-integration-flowdefinition-flowname): String
  [KmsArn](#cfn-customerprofiles-integration-flowdefinition-kmsarn): String
  [SourceFlowConfig](#cfn-customerprofiles-integration-flowdefinition-sourceflowconfig): 
    SourceFlowConfig
  [Tasks](#cfn-customerprofiles-integration-flowdefinition-tasks): 
    - Task
  [TriggerConfig](#cfn-customerprofiles-integration-flowdefinition-triggerconfig): 
    TriggerConfig
```

## Properties<a name="aws-properties-customerprofiles-integration-flowdefinition-properties"></a>

`Description`  <a name="cfn-customerprofiles-integration-flowdefinition-description"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlowName`  <a name="cfn-customerprofiles-integration-flowdefinition-flowname"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsArn`  <a name="cfn-customerprofiles-integration-flowdefinition-kmsarn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFlowConfig`  <a name="cfn-customerprofiles-integration-flowdefinition-sourceflowconfig"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: [SourceFlowConfig](aws-properties-customerprofiles-integration-sourceflowconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tasks`  <a name="cfn-customerprofiles-integration-flowdefinition-tasks"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: List of [Task](aws-properties-customerprofiles-integration-task.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TriggerConfig`  <a name="cfn-customerprofiles-integration-flowdefinition-triggerconfig"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: [TriggerConfig](aws-properties-customerprofiles-integration-triggerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)