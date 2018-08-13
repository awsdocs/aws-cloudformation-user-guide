# Amazon Elastic Container Service TaskDefinition VolumeFrom<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom"></a>

`VolumesFrom` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property that mounts data volumes from other containers\.

## Syntax<a name="w3ab2c21c14d902b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom-syntax.json"></a>

```
{
  "[SourceContainer](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-sourcecontainer)" : String,
  "[ReadOnly](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-readonly)" : Boolean
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom-syntax.yaml"></a>

```
[SourceContainer](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-sourcecontainer): String
[ReadOnly](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-readonly): Boolean
```

## Properties<a name="w3ab2c21c14d902b7"></a>

For more information about each property, see [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`SourceContainer`  <a name="cfn-ecs-taskdefinition-containerdefinition-volumesfrom-sourcecontainer"></a>
The name of the container that has the volumes to mount\.  
*Required*: Yes  
*Type*: String

`ReadOnly`  <a name="cfn-ecs-taskdefinition-containerdefinition-volumesfrom-readonly"></a>
Indicates whether the container can write to the volume\. If you specify **true**, the container has read\-only access to the volume\. If you specify **false**, the container can write to the volume\. By default, the value is **false**\.  
*Required*: No  
*Type*: Boolean