# AWS::ECS::Service PlacementConstraint<a name="aws-properties-ecs-service-placementconstraint"></a>

The `PlacementConstraint` property specifies an object representing a constraint on task placement in the task definition\. For more information, see [Task Placement Constraints](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-constraints.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-service-placementconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-service-placementconstraint-syntax.json"></a>

```
{
  "[Expression](#cfn-ecs-service-placementconstraint-expression)" : String,
  "[Type](#cfn-ecs-service-placementconstraint-type)" : String
}
```

### YAML<a name="aws-properties-ecs-service-placementconstraint-syntax.yaml"></a>

```
  [Expression](#cfn-ecs-service-placementconstraint-expression): String
  [Type](#cfn-ecs-service-placementconstraint-type): String
```

## Properties<a name="aws-properties-ecs-service-placementconstraint-properties"></a>

`Expression`  <a name="cfn-ecs-service-placementconstraint-expression"></a>
A cluster query language expression to apply to the constraint\. You cannot specify an expression if the constraint type is `distinctInstance`\. For more information, see [Cluster Query Language](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/cluster-query-language.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-ecs-service-placementconstraint-type"></a>
The type of constraint\. Use `distinctInstance` to ensure that each task in a particular group is running on a different container instance\. Use `memberOf` to restrict the selection to a group of valid candidates\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `distinctInstance | memberOf`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)