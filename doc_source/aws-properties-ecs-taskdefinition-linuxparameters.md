# AWS::ECS::TaskDefinition LinuxParameters<a name="aws-properties-ecs-taskdefinition-linuxparameters"></a>

The `LinuxParameters` property specifies Linux\-specific options that are applied to the container, such as Linux [KernelCapabilities](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_KernelCapabilities.html)\.

## Syntax<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax.json"></a>

```
{
  "[Capabilities](#cfn-ecs-taskdefinition-linuxparameters-capabilities)" : KernelCapabilities,
  "[Devices](#cfn-ecs-taskdefinition-linuxparameters-devices)" : [ Device, ... ],
  "[InitProcessEnabled](#cfn-ecs-taskdefinition-linuxparameters-initprocessenabled)" : Boolean,
  "[MaxSwap](#cfn-ecs-taskdefinition-linuxparameters-maxswap)" : Integer,
  "[SharedMemorySize](#cfn-ecs-taskdefinition-linuxparameters-sharedmemorysize)" : Integer,
  "[Swappiness](#cfn-ecs-taskdefinition-linuxparameters-swappiness)" : Integer,
  "[Tmpfs](#cfn-ecs-taskdefinition-linuxparameters-tmpfs)" : [ Tmpfs, ... ]
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax.yaml"></a>

```
  [Capabilities](#cfn-ecs-taskdefinition-linuxparameters-capabilities): 
    KernelCapabilities
  [Devices](#cfn-ecs-taskdefinition-linuxparameters-devices): 
    - Device
  [InitProcessEnabled](#cfn-ecs-taskdefinition-linuxparameters-initprocessenabled): Boolean
  [MaxSwap](#cfn-ecs-taskdefinition-linuxparameters-maxswap): Integer
  [SharedMemorySize](#cfn-ecs-taskdefinition-linuxparameters-sharedmemorysize): Integer
  [Swappiness](#cfn-ecs-taskdefinition-linuxparameters-swappiness): Integer
  [Tmpfs](#cfn-ecs-taskdefinition-linuxparameters-tmpfs): 
    - Tmpfs
```

## Properties<a name="aws-properties-ecs-taskdefinition-linuxparameters-properties"></a>

`Capabilities`  <a name="cfn-ecs-taskdefinition-linuxparameters-capabilities"></a>
The Linux capabilities for the container that are added to or dropped from the default configuration provided by Docker\.  
For tasks that use the Fargate launch type, `capabilities` is supported for all platform versions but the `add` parameter is only supported if using platform version 1\.4\.0 or later\.
*Required*: No  
*Type*: [KernelCapabilities](aws-properties-ecs-taskdefinition-kernelcapabilities.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Devices`  <a name="cfn-ecs-taskdefinition-linuxparameters-devices"></a>
Any host devices to expose to the container\. This parameter maps to `Devices` in the [Create a container](https://docs.docker.com/engine/api/v1.35/#operation/ContainerCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `--device` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration)\.  
If you are using tasks that use the Fargate launch type, the `devices` parameter is not supported\.
*Required*: No  
*Type*: List of [Device](aws-properties-ecs-taskdefinition-device.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InitProcessEnabled`  <a name="cfn-ecs-taskdefinition-linuxparameters-initprocessenabled"></a>
Run an `init` process inside the container that forwards signals and reaps processes\. This parameter maps to the `--init` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration)\. This parameter requires version 1\.25 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log in to your container instance and run the following command: `sudo docker version --format '{{.Server.APIVersion}}'`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxSwap`  <a name="cfn-ecs-taskdefinition-linuxparameters-maxswap"></a>
The total amount of swap memory \(in MiB\) a container can use\. This parameter will be translated to the `--memory-swap` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration) where the value would be the sum of the container memory plus the `maxSwap` value\.  
If a `maxSwap` value of `0` is specified, the container will not use swap\. Accepted values are `0` or any positive integer\. If the `maxSwap` parameter is omitted, the container will use the swap configuration for the container instance it is running on\. A `maxSwap` value must be set for the `swappiness` parameter to be used\.  
If you are using tasks that use the Fargate launch type, the `maxSwap` parameter is not supported\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SharedMemorySize`  <a name="cfn-ecs-taskdefinition-linuxparameters-sharedmemorysize"></a>
The value for the size \(in MiB\) of the `/dev/shm` volume\. This parameter maps to the `--shm-size` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration)\.  
If you are using tasks that use the Fargate launch type, the `sharedMemorySize` parameter is not supported\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Swappiness`  <a name="cfn-ecs-taskdefinition-linuxparameters-swappiness"></a>
This allows you to tune a container's memory swappiness behavior\. A `swappiness` value of `0` will cause swapping to not happen unless absolutely necessary\. A `swappiness` value of `100` will cause pages to be swapped very aggressively\. Accepted values are whole numbers between `0` and `100`\. If the `swappiness` parameter is not specified, a default value of `60` is used\. If a value is not specified for `maxSwap` then this parameter is ignored\. This parameter maps to the `--memory-swappiness` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration)\.  
If you are using tasks that use the Fargate launch type, the `swappiness` parameter is not supported\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tmpfs`  <a name="cfn-ecs-taskdefinition-linuxparameters-tmpfs"></a>
The container path, mount options, and size \(in MiB\) of the tmpfs mount\. This parameter maps to the `--tmpfs` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration)\.  
If you are using tasks that use the Fargate launch type, the `tmpfs` parameter is not supported\.
*Required*: No  
*Type*: [List](aws-properties-ecs-taskdefinition-tmpfs.md) of [Tmpfs](aws-properties-ecs-taskdefinition-tmpfs.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)