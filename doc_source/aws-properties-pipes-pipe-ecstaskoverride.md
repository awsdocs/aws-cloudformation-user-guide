# AWS::Pipes::Pipe EcsTaskOverride<a name="aws-properties-pipes-pipe-ecstaskoverride"></a>

The overrides that are associated with a task\.

## Syntax<a name="aws-properties-pipes-pipe-ecstaskoverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-ecstaskoverride-syntax.json"></a>

```
{
  "[ContainerOverrides](#cfn-pipes-pipe-ecstaskoverride-containeroverrides)" : [ EcsContainerOverride, ... ],
  "[Cpu](#cfn-pipes-pipe-ecstaskoverride-cpu)" : String,
  "[EphemeralStorage](#cfn-pipes-pipe-ecstaskoverride-ephemeralstorage)" : EcsEphemeralStorage,
  "[ExecutionRoleArn](#cfn-pipes-pipe-ecstaskoverride-executionrolearn)" : String,
  "[InferenceAcceleratorOverrides](#cfn-pipes-pipe-ecstaskoverride-inferenceacceleratoroverrides)" : [ EcsInferenceAcceleratorOverride, ... ],
  "[Memory](#cfn-pipes-pipe-ecstaskoverride-memory)" : String,
  "[TaskRoleArn](#cfn-pipes-pipe-ecstaskoverride-taskrolearn)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-ecstaskoverride-syntax.yaml"></a>

```
  [ContainerOverrides](#cfn-pipes-pipe-ecstaskoverride-containeroverrides): 
    - EcsContainerOverride
  [Cpu](#cfn-pipes-pipe-ecstaskoverride-cpu): String
  [EphemeralStorage](#cfn-pipes-pipe-ecstaskoverride-ephemeralstorage): 
    EcsEphemeralStorage
  [ExecutionRoleArn](#cfn-pipes-pipe-ecstaskoverride-executionrolearn): String
  [InferenceAcceleratorOverrides](#cfn-pipes-pipe-ecstaskoverride-inferenceacceleratoroverrides): 
    - EcsInferenceAcceleratorOverride
  [Memory](#cfn-pipes-pipe-ecstaskoverride-memory): String
  [TaskRoleArn](#cfn-pipes-pipe-ecstaskoverride-taskrolearn): String
```

## Properties<a name="aws-properties-pipes-pipe-ecstaskoverride-properties"></a>

`ContainerOverrides`  <a name="cfn-pipes-pipe-ecstaskoverride-containeroverrides"></a>
One or more container overrides that are sent to a task\.  
*Required*: No  
*Type*: List of [EcsContainerOverride](aws-properties-pipes-pipe-ecscontaineroverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cpu`  <a name="cfn-pipes-pipe-ecstaskoverride-cpu"></a>
The cpu override for the task\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EphemeralStorage`  <a name="cfn-pipes-pipe-ecstaskoverride-ephemeralstorage"></a>
The ephemeral storage setting override for the task\.  
This parameter is only supported for tasks hosted on Fargate that use the following platform versions:  
+ Linux platform version `1.4.0` or later\.
+ Windows platform version `1.0.0` or later\.
*Required*: No  
*Type*: [EcsEphemeralStorage](aws-properties-pipes-pipe-ecsephemeralstorage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionRoleArn`  <a name="cfn-pipes-pipe-ecstaskoverride-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the task execution IAM role override for the task\. For more information, see [Amazon ECS task execution IAM role](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_execution_IAM_role.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InferenceAcceleratorOverrides`  <a name="cfn-pipes-pipe-ecstaskoverride-inferenceacceleratoroverrides"></a>
The Elastic Inference accelerator override for the task\.  
*Required*: No  
*Type*: List of [EcsInferenceAcceleratorOverride](aws-properties-pipes-pipe-ecsinferenceacceleratoroverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Memory`  <a name="cfn-pipes-pipe-ecstaskoverride-memory"></a>
The memory override for the task\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TaskRoleArn`  <a name="cfn-pipes-pipe-ecstaskoverride-taskrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that containers in this task can assume\. All containers in this task are granted the permissions that are specified in this role\. For more information, see [IAM Role for Tasks](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-iam-roles.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)