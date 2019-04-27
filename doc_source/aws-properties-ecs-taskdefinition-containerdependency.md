# Amazon ECS TaskDefinition ContainerDependency<a name="aws-properties-ecs-taskdefinition-containerdependency"></a>

<a name="aws-properties-ecs-taskdefinition-containerdependency-description"></a>The `ContainerDependency` property type specifies the dependencies defined for container startup and shutdown\. A container can contain multiple dependencies\. When a dependency is defined for container startup, for container shutdown it is reversed\.

Your Amazon ECS container instances require at least version 1\.26\.0 of the container agent to enable container dependencies\. However, we recommend using the latest container agent version\. For information about checking your agent version and updating to the latest version, see [Updating the Amazon ECS Container Agent](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-agent-update.html) in the *Amazon Elastic Container Service Developer Guide*\. If you are using an Amazon ECS\-optimized Linux AMI, your instance needs at least version 1\.26\.0\-1 of the ecs\-init package\. If your container instances are launched from version 20190301 or later, then they contain the required versions of the container agent and ecs\-init\. For more information, see [Amazon ECS\-optimized Linux AMI](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html) in the *Amazon Elastic Container Service Developer Guide*\.

**Note**  
This parameter is available for tasks using the Fargate launch type in the Ohio \(us\-east\-2\) region only and the task or service requires platform version 1\.3\.0 or later\.

<a name="aws-properties-ecs-taskdefinition-containerdependency-inheritance"></a> `ContainerDependency` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property type\.

## Syntax<a name="aws-properties-ecs-taskdefinition-containerdependency-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-containerdependency-syntax.json"></a>

```
{
  "[Condition](#cfn-ecs-taskdefinition-containerdependency-condition)" : String,
  "[ContainerName](#cfn-ecs-taskdefinition-containerdependency-containername)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdependency-syntax.yaml"></a>

```
[Condition](#cfn-ecs-taskdefinition-containerdependency-condition): String
[ContainerName](#cfn-ecs-taskdefinition-containerdependency-containername): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-containerdependency-properties"></a>

`Condition`  <a name="cfn-ecs-taskdefinition-containerdependency-condition"></a>
The dependency condition of the container\. For a full list of available conditions and their behavior, see [ContainerDependency](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDependency.html) in the *Amazon Elastic Container Service API Reference*  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ContainerName`  <a name="cfn-ecs-taskdefinition-containerdependency-containername"></a>
The name of a container\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 