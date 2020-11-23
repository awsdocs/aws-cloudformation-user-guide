# AWS::ECS::PrimaryTaskSet<a name="aws-resource-ecs-primarytaskset"></a>

Specifies which task set in a service is the primary task set\. Any parameters that are updated on the primary task set in a service will transition to the service\. This is used when a service uses the `EXTERNAL` deployment controller type\. For more information, see [Amazon ECS Deployment Types](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-types.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-resource-ecs-primarytaskset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-primarytaskset-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::PrimaryTaskSet",
  "Properties" : {
      "[Cluster](#cfn-ecs-primarytaskset-cluster)" : String,
      "[Service](#cfn-ecs-primarytaskset-service)" : String,
      "[TaskSetId](#cfn-ecs-primarytaskset-tasksetid)" : String
    }
}
```

### YAML<a name="aws-resource-ecs-primarytaskset-syntax.yaml"></a>

```
Type: AWS::ECS::PrimaryTaskSet
Properties: 
  [Cluster](#cfn-ecs-primarytaskset-cluster): String
  [Service](#cfn-ecs-primarytaskset-service): String
  [TaskSetId](#cfn-ecs-primarytaskset-tasksetid): String
```

## Properties<a name="aws-resource-ecs-primarytaskset-properties"></a>

`Cluster`  <a name="cfn-ecs-primarytaskset-cluster"></a>
The short name or full Amazon Resource Name \(ARN\) of the cluster that hosts the service that the task set exists in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Service`  <a name="cfn-ecs-primarytaskset-service"></a>
The short name or full Amazon Resource Name \(ARN\) of the service that the task set exists in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TaskSetId`  <a name="cfn-ecs-primarytaskset-tasksetid"></a>
The short name or full Amazon Resource Name \(ARN\) of the task set to set as the primary task set in the deployment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ecs-primarytaskset-return-values"></a>

### Ref<a name="aws-resource-ecs-primarytaskset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.