# AWS::ECS::TaskDefinition TaskDefinitionPlacementConstraint<a name="aws-properties-ecs-taskdefinition-taskdefinitionplacementconstraint"></a>

The `TaskDefinitionPlacementConstraint` property specifies an object representing a constraint on task placement in the task definition\.

If you are using the Fargate launch type, task placement constraints are not supported\.

For more information, see [Task Placement Constraints](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-constraints.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-taskdefinition-taskdefinitionplacementconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-taskdefinitionplacementconstraint-syntax.json"></a>

```
{
  "[Expression](#cfn-ecs-taskdefinition-taskdefinitionplacementconstraint-expression)" : String,
  "[Type](#cfn-ecs-taskdefinition-taskdefinitionplacementconstraint-type)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-taskdefinitionplacementconstraint-syntax.yaml"></a>

```
  [Expression](#cfn-ecs-taskdefinition-taskdefinitionplacementconstraint-expression): String
  [Type](#cfn-ecs-taskdefinition-taskdefinitionplacementconstraint-type): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-taskdefinitionplacementconstraint-properties"></a>

`Expression`  <a name="cfn-ecs-taskdefinition-taskdefinitionplacementconstraint-expression"></a>
A cluster query language expression to apply to the constraint\. For more information, see [Cluster Query Language](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/cluster-query-language.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-ecs-taskdefinition-taskdefinitionplacementconstraint-type"></a>
The type of constraint\. The `MemberOf` constraint restricts selection to be from a group of valid candidates\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `memberOf`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)