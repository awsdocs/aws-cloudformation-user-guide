# AWS::ECS::TaskDefinition ResourceRequirement<a name="aws-properties-ecs-taskdefinition-resourcerequirement"></a>

The `ResourceRequirement` property specifies the type and amount of a resource to assign to a container\. The only supported resource is a GPU\. For more information, see [Working with GPUs on Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-gpu.html) in the *Amazon Elastic Container Service Developer Guide* 

## Syntax<a name="aws-properties-ecs-taskdefinition-resourcerequirement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-resourcerequirement-syntax.json"></a>

```
{
  "[Type](#cfn-ecs-taskdefinition-resourcerequirement-type)" : String,
  "[Value](#cfn-ecs-taskdefinition-resourcerequirement-value)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-resourcerequirement-syntax.yaml"></a>

```
  [Type](#cfn-ecs-taskdefinition-resourcerequirement-type): String
  [Value](#cfn-ecs-taskdefinition-resourcerequirement-value): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-resourcerequirement-properties"></a>

`Type`  <a name="cfn-ecs-taskdefinition-resourcerequirement-type"></a>
The type of resource to assign to a container\. The supported values are `GPU` or `InferenceAccelerator`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `GPU | InferenceAccelerator`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-ecs-taskdefinition-resourcerequirement-value"></a>
The value for the specified resource type\.  
If the `GPU` type is used, the value is the number of physical `GPUs` the Amazon ECS container agent will reserve for the container\. The number of GPUs reserved for all containers in a task should not exceed the number of available GPUs on the container instance the task is launched on\.  
If the `InferenceAccelerator` type is used, the `value` should match the `DeviceName` for an [InferenceAccelerator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-inferenceaccelerator.html) specified in a task definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)