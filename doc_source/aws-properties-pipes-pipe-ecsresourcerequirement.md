# AWS::Pipes::Pipe EcsResourceRequirement<a name="aws-properties-pipes-pipe-ecsresourcerequirement"></a>

The type and amount of a resource to assign to a container\. The supported resource types are GPUs and Elastic Inference accelerators\. For more information, see [Working with GPUs on Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-gpu.html) or [Working with Amazon Elastic Inference on Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-inference.html) in the *Amazon Elastic Container Service Developer Guide*

## Syntax<a name="aws-properties-pipes-pipe-ecsresourcerequirement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-ecsresourcerequirement-syntax.json"></a>

```
{
  "[Type](#cfn-pipes-pipe-ecsresourcerequirement-type)" : String,
  "[Value](#cfn-pipes-pipe-ecsresourcerequirement-value)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-ecsresourcerequirement-syntax.yaml"></a>

```
  [Type](#cfn-pipes-pipe-ecsresourcerequirement-type): String
  [Value](#cfn-pipes-pipe-ecsresourcerequirement-value): String
```

## Properties<a name="aws-properties-pipes-pipe-ecsresourcerequirement-properties"></a>

`Type`  <a name="cfn-pipes-pipe-ecsresourcerequirement-type"></a>
The type of resource to assign to a container\. The supported values are `GPU` or `InferenceAccelerator`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-pipes-pipe-ecsresourcerequirement-value"></a>
The value for the specified resource type\.  
If the `GPU` type is used, the value is the number of physical `GPUs` the Amazon ECS container agent reserves for the container\. The number of GPUs that's reserved for all containers in a task can't exceed the number of available GPUs on the container instance that the task is launched on\.  
If the `InferenceAccelerator` type is used, the `value` matches the `deviceName` for an InferenceAccelerator specified in a task definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)