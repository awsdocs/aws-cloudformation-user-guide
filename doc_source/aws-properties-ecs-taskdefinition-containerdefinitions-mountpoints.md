# Amazon Elastic Container Service TaskDefinition MountPoint<a name="aws-properties-ecs-taskdefinition-containerdefinitions-mountpoints"></a>

`MountPoints` is a property of the [Amazon Elastic Container Service TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property that specifies the mount points for data volumes in a container\.

## Syntax<a name="w3ab2c21c14d890b5"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-mountpoints-syntax.json"></a>

```
{
  "[ContainerPath](#cfn-ecs-taskdefinition-containerdefinition-mountpoints-containerpath)" : String,
  "[SourceVolume](#cfn-ecs-taskdefinition-containerdefinition-mountpoints-sourcevolume)" : String,
  "[ReadOnly](#cfn-ecs-taskdefinition-containerdefinition-mountpoints-readonly)" : Boolean
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-mountpoints-syntax.yaml"></a>

```
[ContainerPath](#cfn-ecs-taskdefinition-containerdefinition-mountpoints-containerpath): String
[SourceVolume](#cfn-ecs-taskdefinition-containerdefinition-mountpoints-sourcevolume): String
[ReadOnly](#cfn-ecs-taskdefinition-containerdefinition-mountpoints-readonly): Boolean
```

## Properties<a name="w3ab2c21c14d890b7"></a>

For more information about each property, see [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`ContainerPath`  <a name="cfn-ecs-taskdefinition-containerdefinition-mountpoints-containerpath"></a>
The path on the container that indicates where you want to mount the volume\.  
*Required*: Yes  
*Type*: String

`SourceVolume`  <a name="cfn-ecs-taskdefinition-containerdefinition-mountpoints-sourcevolume"></a>
The name of the volume to mount\.  
*Required*: Yes  
*Type*: String

`ReadOnly`  <a name="cfn-ecs-taskdefinition-containerdefinition-mountpoints-readonly"></a>
Indicates whether the container can write to the volume\. If you specify **true**, the container has read\-only access to the volume\. If you specify **false**, the container can write to the volume\. By default, the value is **false**\.  
*Required*: No  
*Type*: Boolean