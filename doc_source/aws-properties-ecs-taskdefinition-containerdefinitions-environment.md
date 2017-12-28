# Amazon Elastic Container Service TaskDefinition KeyValuePair<a name="aws-properties-ecs-taskdefinition-containerdefinitions-environment"></a>

`Environment` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property that specifies environment variables for a container\.

## Syntax<a name="w3ab2c21c14d696b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-environment-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-containerdefinition-environment-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-containerdefinition-environment-value)" : String 
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-environment-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-containerdefinition-environment-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-containerdefinition-environment-value): String
```

## Properties<a name="w3ab2c21c14d696b7"></a>

For more information about each property, see [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`Name`  
The name of the environment variable\.  
*Required: *Yes  
*Type*: String

`Value`  
The value of the environment variable\.  
*Required: *Yes  
*Type*: String