# AWS::ECS::Cluster<a name="aws-resource-ecs-cluster"></a>

The `AWS::ECS::Cluster` resource creates an Amazon Elastic Container Service \(Amazon ECS\) cluster\.

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
Type: AWS::ECS::Cluster
Properties: 
  [ClusterName](#cfn-ecs-cluster-clustername): String
```

## Properties<a name="aws-resource-ecs-cluster-properties"></a>

`ClusterName`  <a name="cfn-ecs-cluster-clustername"></a>
A user\-generated string that you use to identify your cluster\. If you don't specify a name, AWS CloudFormation generates a unique physical ID for the name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-ecs-cluster-return-values"></a>

### Ref<a name="aws-resource-ecs-cluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

In the following example, the `Ref` function returns the name of the `MyECSCluster` cluster, such as `MyStack-MyECSCluster-NT5EUXTNTXXD`\.

 `{ "Ref": "MyECSCluster" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ecs-cluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ecs-cluster-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Amazon ECS cluster, such as `arn:aws:ecs:us-east-2:123456789012:cluster/MyECSCluster`\.

## Examples<a name="aws-resource-ecs-cluster--examples"></a>

### Creating an Amazon ECS cluster<a name="aws-resource-ecs-cluster--examples--Creating_an_Amazon_ECS_cluster"></a>

The following sample declares an Amazon ECS cluster:

#### JSON<a name="aws-resource-ecs-cluster--examples--Creating_an_Amazon_ECS_cluster--json"></a>

```
"MyCluster": {
  "Type": "AWS::ECS::Cluster"
}
```

#### YAML<a name="aws-resource-ecs-cluster--examples--Creating_an_Amazon_ECS_cluster--yaml"></a>

```
MyCluster:
  Type: AWS::ECS::Cluster
```