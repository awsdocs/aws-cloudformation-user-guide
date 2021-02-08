# AWS::Detective::Graph<a name="aws-resource-detective-graph"></a>

The `AWS::Detective::Graph` resource is an Amazon Detective resource type that creates a Detective behavior graph\. The requesting account becomes the master account for the behavior graph\.

## Syntax<a name="aws-resource-detective-graph-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-detective-graph-syntax.json"></a>

```
{
  "Type" : "AWS::Detective::Graph",
  "Properties" : {
    }
}
```

### YAML<a name="aws-resource-detective-graph-syntax.yaml"></a>

```
Type: AWS::Detective::Graph
Properties:
```

## Return values<a name="aws-resource-detective-graph-return-values"></a>

### Ref<a name="aws-resource-detective-graph-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the new behavior graph\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-detective-graph-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-detective-graph-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the new behavior graph\.

## Examples<a name="aws-resource-detective-graph--examples"></a>

### Creating a new Detective behavior graph<a name="aws-resource-detective-graph--examples--Creating_a_new_Detective_behavior_graph"></a>

This example shows how to declare a new `AWS:Detective:Graph` resource to create a new Detective behavior graph

#### JSON<a name="aws-resource-detective-graph--examples--Creating_a_new_Detective_behavior_graph--json"></a>

```
"NewGraph": {
    "Type": "AWS::Detective::Graph"
}
```

#### YAML<a name="aws-resource-detective-graph--examples--Creating_a_new_Detective_behavior_graph--yaml"></a>

```
NewGraph:
    Type: AWS::Detective::Graph
```