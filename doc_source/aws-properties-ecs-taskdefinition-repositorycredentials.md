# Amazon ECS TaskDefinition RepositoryCredentials<a name="aws-properties-ecs-taskdefinition-repositorycredentials"></a>

<a name="aws-properties-ecs-taskdefinition-repositorycredentials-description"></a>The `RepositoryCredentials` property type specifies the repository credentials for private registry authentication\.

<a name="aws-properties-ecs-taskdefinition-repositorycredentials-inheritance"></a> `RepositoryCredentials` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property type\.

## Syntax<a name="aws-properties-ecs-taskdefinition-repositorycredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-repositorycredentials-syntax.json"></a>

```
{
  "[CredentialsParameter](#cfn-ecs-taskdefinition-repositorycredentials-credentialsparameter)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-repositorycredentials-syntax.yaml"></a>

```
[CredentialsParameter](#cfn-ecs-taskdefinition-repositorycredentials-credentialsparameter): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-repositorycredentials-properties"></a>

`CredentialsParameter`  <a name="cfn-ecs-taskdefinition-repositorycredentials-credentialsparameter"></a>
The Amazon Resource Name \(ARN\) of the secret containing the private repository credentials\.  
When using the Amazon ECS API, AWS CLI, or AWS SDK, if the secret exists in the same region as the task you are launching then you can use either the full ARN or name of the secret\. When using the AWS Management Console, the full ARN of the secret must be specified\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-ecs-taskdefinition-repositorycredentials-seealso"></a>
+ [RepositoryCredentials](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_RepositoryCredentials.html) in the *Amazon Elastic Container Service API Reference*