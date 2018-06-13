# Amazon Elastic Container Service Service PlacementConstraint<a name="aws-properties-ecs-taskdefinition-placementconstraints-taskdefinitionplacementconstraint"></a>

`PlacementConstraint` is a property of the [AWS::ECS::Service](aws-resource-ecs-service.md) resource that specifies the placement constraints for the tasks in the service to associate with an Amazon Elastic Container Service \(Amazon ECS\) service\.

## Syntax<a name="w3ab2c21c14d906b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-placementconstraints-taskdefinitionplacementconstraint-syntax.json"></a>

```
{
  "[Type](#cfn-ecs-service-placementconstraints-placementconstraint-type)" : String,
  "[Expression](#cfn-ecs-service-placementconstraints-placementconstraint-expression)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-placementconstraints-taskdefinitionplacementconstraint-syntax.yaml"></a>

```
[Type](#cfn-ecs-service-placementconstraints-placementconstraint-type): String
[Expression](#cfn-ecs-service-placementconstraints-placementconstraint-expression): String
```

## Properties<a name="w3ab2c21c14d906b7"></a>

`Type`  <a name="cfn-ecs-service-placementconstraints-placementconstraint-type"></a>
The type of constraint: `distinctInstance` or `memberOf`\.  
To ensure that each task in a particular group is running on a different container instance, use `distinctInstance`\. To restrict selection to a group of valid candidates, use `memberOf`\. `distinctInstance` is not supported in task definitions\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Expression`  <a name="cfn-ecs-service-placementconstraints-placementconstraint-expression"></a>
A cluster query language expression to apply to the constraint\. If the constraint type is `distinctInstance`, you can't specify an expression\. For more information, see [Cluster Query Language](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/cluster-query-language.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)