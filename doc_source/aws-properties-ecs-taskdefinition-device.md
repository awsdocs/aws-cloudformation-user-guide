# Amazon Elastic Container Service TaskDefinition Device<a name="aws-properties-ecs-taskdefinition-device"></a>

<a name="aws-properties-ecs-taskdefinition-device-description"></a>The `Device` property type specifies a device on a host container instance\.

<a name="aws-properties-ecs-taskdefinition-device-inheritance"></a> The `Devices` property of the [Amazon ECS TaskDefinition LinuxParameters](aws-properties-ecs-taskdefinition-linuxparameters.md) contains a list of `Device` property types\.

## Syntax<a name="aws-properties-ecs-taskdefinition-device-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-device-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-device-containerpath)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-device-hostpath)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-device-permissions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-device-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-device-containerpath): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-device-hostpath): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ecs-taskdefinition-device-permissions): 
  - String
```

## Properties<a name="aws-properties-ecs-taskdefinition-device-properties"></a>

`ContainerPath`  
The path inside the container to expose the host device to\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`HostPath`  
The path for the device on the host container instance\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

`Permissions`  
The explicit permissions to provide to the container for the device\. By default, the container is able to `read`, `write`, and `mknod` the device\.  
 *Required*: No  
 *Type*: List of String values  
 *Valid values*: `read`, `write`, and `mknod`  
 *Update requires*: Replacement 