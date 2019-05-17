# AWS::ECS::TaskDefinition RepositoryCredentials<a name="aws-properties-ecs-taskdefinition-repositorycredentials"></a>

The `RepositoryCredentials` property specifies the repository credentials for private registry authentication\.

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
When you are using the Amazon ECS API, AWS CLI, or AWS SDK, if the secret exists in the same Region as the task that you are launching then you can use either the full ARN or the name of the secret\. When you are using the AWS Management Console, you must specify the full ARN of the secret\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)