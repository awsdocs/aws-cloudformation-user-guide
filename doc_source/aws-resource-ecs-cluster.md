# AWS::ECS::Cluster<a name="aws-resource-ecs-cluster"></a>

The `AWS::ECS::Cluster` resource creates an Amazon Elastic Container Service \(Amazon ECS\) cluster\. This resource has no properties; use the Amazon ECS container agent to connect to the cluster\. For more information, see [Amazon ECS Container Agent](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//ECS_agent.html) in the *Amazon Elastic Container Service Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-ecs-cluster-syntax)
+ [Properties](#aws-resource-servicename-cluster-properties)
+ [Return Values](#aws-resource-ecs-cluster-returnvalues)
+ [Example](#w3ab2c21c10d559c13)

## Syntax<a name="aws-resource-ecs-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::Cluster",
  "Properties" : {
    "[ClusterName](#cfn-ecs-cluster-clustername)" : String
  }
}
```

### YAML<a name="aws-resource-ecs-cluster-syntax.yaml"></a>

```
Type: "AWS::ECS::Cluster"
Properties:
  [ClusterName](#cfn-ecs-cluster-clustername): String
```

## Properties<a name="aws-resource-servicename-cluster-properties"></a>

`ClusterName`  <a name="cfn-ecs-cluster-clustername"></a>
A name for the cluster\. If you don't specify a name, AWS CloudFormation generates a unique physical ID for the name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-ecs-cluster-returnvalues"></a>

### Ref<a name="aws-resource-ecs-cluster-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

In the following sample, the `Ref` function returns the name of the `MyECSCluster` cluster, such as `MyStack-MyECSCluster-NT5EUXTNTXXD`\.

```
{ "Ref": "MyECSCluster" }
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-ecs-cluster-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the Amazon ECS cluster, such as `arn:aws:ecs:us-east-2:123456789012:cluster/MyECSCluster`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w3ab2c21c10d559c13"></a>

The following sample declares an Amazon ECS cluster:

### JSON<a name="aws-resource-ecs-cluster-example.json"></a>

```
"MyCluster": {
  "Type": "AWS::ECS::Cluster"
}
```

### YAML<a name="aws-resource-ecs-cluster-example.yaml"></a>

```
MyCluster:
  Type: "AWS::ECS::Cluster"
```