# Amazon Elastic Container Service Service PlacementStrategies<a name="aws-properties-ecs-service-placementstrategies-placementstrategy"></a>

The `PlacementStrategies` property describes how tasks for the Amazon Elastic Container Service \(Amazon ECS\) service are placed in an `AWS::ECS::Service` resource\.

## Syntax<a name="w3ab2c21c14d849b5"></a>

### JSON<a name="aws-properties-ecs-serviceplacementstrategies-placementstrategy-syntax.json"></a>

```
{
  "[Type](#cfn-ecs-serviceplacementstrategies-placementstrategy-type)" : String,
  "[Field](#cfn-ecs-serviceplacementstrategies-placementstrategy-field)" : String,
}
```

### YAML<a name="aws-properties-ecs-serviceplacementstrategies-placementstrategy-syntax.yaml"></a>

```
[Type](#cfn-ecs-serviceplacementstrategies-placementstrategy-type): String
[Field](#cfn-ecs-serviceplacementstrategies-placementstrategy-field): String
```

## Properties<a name="w3ab2c21c14d849b7"></a>

`Type`  <a name="cfn-ecs-serviceplacementstrategies-placementstrategy-type"></a>
The type of placement strategy\. Can be one of the following values: `random`, `spread`, or `binpack`\.  
The `random` placement strategy randomly places tasks on available candidates\. The `spread` placement strategy spreads placement across available candidates evenly based on the field parameter\. The `binpack` strategy places tasks on available candidates that have the least available amount of the resource that is specified with the field parameter\. For example, if you `binpack` on memory, a task is placed on the instance with the least amount of remaining memory \(but still enough to run the task\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Field`  <a name="cfn-ecs-serviceplacementstrategies-placementstrategy-field"></a>
The field to apply the placement strategy against\. For the `spread` placement strategy, valid values are `instanceId` \(or `host`, which has the same effect\), or any platform or custom attribute that is applied to a container instance, such as `attribute:ecs.availability-zone`\.  
For the `binpack` placement strategy, valid values are `cpu` and `memory`\.  
For the `random` placement strategy, this field is not used\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)