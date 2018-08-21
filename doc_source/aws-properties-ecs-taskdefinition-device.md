# Amazon Elastic Container Service TaskDefinition Device<a name="aws-properties-ecs-taskdefinition-device"></a>

<a name="aws-properties-ecs-taskdefinition-device-description"></a>The `Device` property type specifies a device on a host container instance\.

<a name="aws-properties-ecs-taskdefinition-device-inheritance"></a> The `Devices` property of the [Amazon ECS TaskDefinition LinuxParameters](aws-properties-ecs-taskdefinition-linuxparameters.md) contains a list of `Device` property types\.

## Syntax<a name="aws-properties-ecs-taskdefinition-device-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-device-syntax.json"></a>

```
{
  "[ContainerPath](#cfn-ecs-taskdefinition-device-containerpath)" : String,
  "[HostPath](#cfn-ecs-taskdefinition-device-hostpath)" : String,
  "[Permissions](#cfn-ecs-taskdefinition-device-permissions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-device-syntax.yaml"></a>

```
[ContainerPath](#cfn-ecs-taskdefinition-device-containerpath): String
[HostPath](#cfn-ecs-taskdefinition-device-hostpath): String
[Permissions](#cfn-ecs-taskdefinition-device-permissions): 
  - String
```

## Properties<a name="aws-properties-ecs-taskdefinition-device-properties"></a>

`ContainerPath`  <a name="cfn-ecs-taskdefinition-device-containerpath"></a>
The path inside the container to expose the host device to\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`HostPath`  <a name="cfn-ecs-taskdefinition-device-hostpath"></a>
The path for the device on the host container instance\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Permissions`  <a name="cfn-ecs-taskdefinition-device-permissions"></a>
The explicit permissions to provide to the container for the device\. By default, the container is able to `read`, `write`, and `mknod` the device\.  
 *Required*: No  
 *Type*: List of String values  
 *Valid values*: `read`, `write`, and `mknod`  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 