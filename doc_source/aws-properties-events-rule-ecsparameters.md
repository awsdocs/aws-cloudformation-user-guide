# AWS::Events::Rule EcsParameters<a name="aws-properties-events-rule-ecsparameters"></a>

The `EcsParameters` property type specifies custom parameters to be used when the target is an Amazon ECS task\.

 `EcsParameters` is a property of the [Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html) property type\.

## Syntax<a name="aws-properties-events-rule-ecsparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-ecsparameters-syntax.json"></a>

```
{
  "[TaskCount](#cfn-events-rule-ecsparameters-taskcount)" : Integer,
  "[TaskDefinitionArn](#cfn-events-rule-ecsparameters-taskdefinitionarn)" : String
}
```

### YAML<a name="aws-properties-events-rule-ecsparameters-syntax.yaml"></a>

```
﻿  [TaskCount](#cfn-events-rule-ecsparameters-taskcount) : Integer
﻿  [TaskDefinitionArn](#cfn-events-rule-ecsparameters-taskdefinitionarn) : String
```

## Properties<a name="aws-properties-events-rule-ecsparameters-properties"></a>

`TaskCount`  <a name="cfn-events-rule-ecsparameters-taskcount"></a>
The number of tasks to create based on `TaskDefinition`\. The default is 1\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskDefinitionArn`  <a name="cfn-events-rule-ecsparameters-taskdefinitionarn"></a>
The ARN of the task definition to use\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)