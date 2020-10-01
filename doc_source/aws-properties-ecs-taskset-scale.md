# AWS::ECS::TaskSet Scale<a name="aws-properties-ecs-taskset-scale"></a>

A floating\-point percentage of the desired number of tasks to place and keep running in the task set\.

## Syntax<a name="aws-properties-ecs-taskset-scale-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskset-scale-syntax.json"></a>

```
{
  "[Unit](#cfn-ecs-taskset-scale-unit)" : String,
  "[Value](#cfn-ecs-taskset-scale-value)" : Double
}
```

### YAML<a name="aws-properties-ecs-taskset-scale-syntax.yaml"></a>

```
  [Unit](#cfn-ecs-taskset-scale-unit): String
  [Value](#cfn-ecs-taskset-scale-value): Double
```

## Properties<a name="aws-properties-ecs-taskset-scale-properties"></a>

`Unit`  <a name="cfn-ecs-taskset-scale-unit"></a>
The unit of measure for the scale value\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PERCENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-ecs-taskset-scale-value"></a>
The value, specified as a percent total of a service's `desiredCount`, to scale the task set\. Accepted values are numbers between 0 and 100\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)