# Amazon CloudWatch Events Rule EcsParameters<a name="aws-properties-events-rule-ecsparameters"></a>

<a name="aws-properties-events-rule-ecsparameters-description"></a>The `EcsParameters` property type specifies information about an Amazon Elastic Container Service \(Amazon ECS\) task target\.

<a name="aws-properties-events-rule-ecsparameters-inheritance"></a> `EcsParameters` is a property of the [CloudWatch Events Rule Target](aws-properties-events-rule-target.md) property type\. 

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
[TaskCount](#cfn-events-rule-ecsparameters-taskcount): Integer
[TaskDefinitionArn](#cfn-events-rule-ecsparameters-taskdefinitionarn): String
```

## Properties<a name="aws-properties-events-rule-ecsparameters-properties"></a>

For more information, including constraints and valid values, see [EcsParameters](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_EcsParameters.html) in the *Amazon CloudWatch Events API Reference*\.

`TaskCount`  <a name="cfn-events-rule-ecsparameters-taskcount"></a>
The number of tasks to create based on the task definition\. The default is `1`\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TaskDefinitionArn`  <a name="cfn-events-rule-ecsparameters-taskdefinitionarn"></a>
The Amazon Resource Name \(ARN\) of the task definition to use\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 