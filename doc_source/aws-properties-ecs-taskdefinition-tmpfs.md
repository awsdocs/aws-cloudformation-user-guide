# Amazon ECS TaskDefinition Tmpfs<a name="aws-properties-ecs-taskdefinition-tmpfs"></a>

<a name="aws-properties-ecs-taskdefinition-tmpfs-description"></a>The `Tmpfs` property type specifies the container path, mount options, and size of the tmpfs mount\.

<a name="aws-properties-ecs-taskdefinition-tmpfs-inheritance"></a> `Tmpfs` is a property of the [Amazon Elastic Container Service TaskDefinition LinuxParameters](aws-properties-ecs-taskdefinition-linuxparameters.md) property type\.

## Syntax<a name="aws-properties-ecs-taskdefinition-tmpfs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-tmpfs-syntax.json"></a>

```
{
  "[ContainerPath](#cfn-ecs-taskdefinition-tmpfs-containerpath)" : String,
  "[MountOptions](#cfn-ecs-taskdefinition-tmpfs-mountoptions)" : [ String, ... ] ,
  "[Size](#cfn-ecs-taskdefinition-tmpfs-size)" : Integer
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-tmpfs-syntax.yaml"></a>

```
[ContainerPath](#cfn-ecs-taskdefinition-tmpfs-containerpath): String
[MountOptions](#cfn-ecs-taskdefinition-tmpfs-mountoptions)
  - String
[Size](#cfn-ecs-taskdefinition-tmpfs-size): Integer
```

## Properties<a name="aws-properties-ecs-taskdefinition-tmpfs-properties"></a>

`ContainerPath`  <a name="cfn-ecs-taskdefinition-tmpfs-containerpath"></a>
The absolute file path where the tmpfs volume is to be mounted\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`MountOptions`  <a name="cfn-ecs-taskdefinition-tmpfs-mountoptions"></a>
The list of tmpfs volume mount options\. For a complete list of valid values, see [Tmpfs](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_Tmpfs.html) in the *Amazon Elastic Container Service API Reference*\.  
Duplicate values are not allowed\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Size`  <a name="cfn-ecs-taskdefinition-tmpfs-size"></a>
The size \(in MiB\) of the tmpfs volume\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-ecs-taskdefinition-tmpfs-seealso"></a>
+ [Tmpfs](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_Tmpfs.html) in the *Amazon Elastic Container Service API Reference*