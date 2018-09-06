# Amazon Elastic Container Service TaskDefinition Ulimit<a name="aws-properties-ecs-taskdefinition-containerdefinitions-ulimit"></a>

`Ulimit` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property that specifies resource limits for an Amazon Elastic Container Service \(Amazon ECS\) container\.

## Syntax<a name="w3ab2c21c14d898b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-ulimit-syntax.json"></a>

```
{
  "[HardLimit](#cfn-ecs-taskdefinition-containerdefinition-ulimit-hardlimit)" : Integer,
  "[Name](#cfn-ecs-taskdefinition-containerdefinition-ulimit-name)" : String,
  "[SoftLimit](#cfn-ecs-taskdefinition-containerdefinition-ulimit-softlimit)" : Integer
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-ulimit-syntax.yaml"></a>

```
[HardLimit](#cfn-ecs-taskdefinition-containerdefinition-ulimit-hardlimit): Integer
[Name](#cfn-ecs-taskdefinition-containerdefinition-ulimit-name): String
[SoftLimit](#cfn-ecs-taskdefinition-containerdefinition-ulimit-softlimit): Integer
```

## Properties<a name="w3ab2c21c14d898b7"></a>

`HardLimit`  <a name="cfn-ecs-taskdefinition-containerdefinition-ulimit-hardlimit"></a>
The hard limit for the ulimit type\.  
*Required*: Yes  
*Type*: Integer

`Name`  <a name="cfn-ecs-taskdefinition-containerdefinition-ulimit-name"></a>
The type of ulimit\. For valid values, see the `name` content for the [Ulimit](http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_Ulimit.html) data type in the *Amazon Elastic Container Service API Reference*\.  
*Required*: No  
*Type*: String

`SoftLimit`  <a name="cfn-ecs-taskdefinition-containerdefinition-ulimit-softlimit"></a>
The soft limit for the ulimit type\.  
*Required*: Yes  
*Type*: Integer