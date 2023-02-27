# AWS::Pipes::Pipe PlacementConstraint<a name="aws-properties-pipes-pipe-placementconstraint"></a>

An object representing a constraint on task placement\. To learn more, see [Task Placement Constraints](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-placement-constraints.html) in the Amazon Elastic Container Service Developer Guide\.

## Syntax<a name="aws-properties-pipes-pipe-placementconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-placementconstraint-syntax.json"></a>

```
{
  "[Expression](#cfn-pipes-pipe-placementconstraint-expression)" : String,
  "[Type](#cfn-pipes-pipe-placementconstraint-type)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-placementconstraint-syntax.yaml"></a>

```
  [Expression](#cfn-pipes-pipe-placementconstraint-expression): String
  [Type](#cfn-pipes-pipe-placementconstraint-type): String
```

## Properties<a name="aws-properties-pipes-pipe-placementconstraint-properties"></a>

`Expression`  <a name="cfn-pipes-pipe-placementconstraint-expression"></a>
A cluster query language expression to apply to the constraint\. You cannot specify an expression if the constraint type is `distinctInstance`\. To learn more, see [Cluster Query Language](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/cluster-query-language.html) in the Amazon Elastic Container Service Developer Guide\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-pipes-pipe-placementconstraint-type"></a>
The type of constraint\. Use distinctInstance to ensure that each task in a particular group is running on a different container instance\. Use memberOf to restrict the selection to a group of valid candidates\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)