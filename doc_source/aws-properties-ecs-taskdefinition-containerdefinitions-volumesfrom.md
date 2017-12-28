# Amazon Elastic Container Service TaskDefinition VolumeFrom<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom"></a>

`VolumesFrom` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property that mounts data volumes from other containers\.

## Syntax<a name="w3ab2c21c14d719b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-sourcecontainer)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-readonly)" : Boolean
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-sourcecontainer): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-readonly): Boolean
```

## Properties<a name="w3ab2c21c14d719b7"></a>

For more information about each property, see [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`SourceContainer`  
The name of the container that has the volumes to mount\.  
*Required: *Yes  
*Type*: String

`ReadOnly`  
Indicates whether the container can write to the volume\. If you specify **true**, the container has read\-only access to the volume\. If you specify **false**, the container can write to the volume\. By default, the value is **false**\.  
*Required: *No  
*Type*: Boolean