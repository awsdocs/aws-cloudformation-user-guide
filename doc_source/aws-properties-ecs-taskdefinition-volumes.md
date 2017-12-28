# Amazon Elastic Container Service TaskDefinition Volumes<a name="aws-properties-ecs-taskdefinition-volumes"></a>

`Volumes` is a property of the [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md) resource that specifies a list of data volumes, which your containers can then access\.

## Syntax<a name="w3ab2c21c14d727b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-volumes-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-volumes-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-volumes-host)" : Host
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-volumes-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-volumes-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-volumes-host):
  Host
```

## Properties<a name="w3ab2c21c14d727b7"></a>

For more information about each property, see [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`Name`  
The name of the volume\. To specify mount points in your container definitions, use the value of this property\.  
*Required: *Yes  
*Type*: String

`Host`  
Determines whether your data volume persists on the host container instance and at the location where it is stored\.  
*Required: *No  
*Type*: [Amazon Elastic Container Service TaskDefinition Volumes Host](aws-properties-ecs-taskdefinition-volumes-host.md)