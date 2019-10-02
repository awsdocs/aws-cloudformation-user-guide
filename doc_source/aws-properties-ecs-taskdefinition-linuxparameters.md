# AWS::ECS::TaskDefinition LinuxParameters<a name="aws-properties-ecs-taskdefinition-linuxparameters"></a>

The `LinuxParameters` property specifies Linux\-specific options that are applied to the container, such as Linux [KernelCapabilities](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_KernelCapabilities.html)\.

## Syntax<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax.json"></a>

```
{
  "[Capabilities](#cfn-ecs-taskdefinition-linuxparameters-capabilities)" : [KernelCapabilities](aws-properties-ecs-taskdefinition-kernelcapabilities.md),
  "[Devices](#cfn-ecs-taskdefinition-linuxparameters-devices)" : [ [Device](aws-properties-ecs-taskdefinition-device.md), ... ],
  "[InitProcessEnabled](#cfn-ecs-taskdefinition-linuxparameters-initprocessenabled)" : Boolean,
  "[SharedMemorySize](#cfn-ecs-taskdefinition-linuxparameters-sharedmemorysize)" : Integer,
  "[Tmpfs](#cfn-ecs-taskdefinition-linuxparameters-tmpfs)" : [ [Tmpfs](aws-properties-ecs-taskdefinition-tmpfs.md), ... ]
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-linuxparameters-syntax.yaml"></a>

```
  [Capabilities](#cfn-ecs-taskdefinition-linuxparameters-capabilities): 
    [KernelCapabilities](aws-properties-ecs-taskdefinition-kernelcapabilities.md)
  [Devices](#cfn-ecs-taskdefinition-linuxparameters-devices): 
    - [Device](aws-properties-ecs-taskdefinition-device.md)
  [InitProcessEnabled](#cfn-ecs-taskdefinition-linuxparameters-initprocessenabled): Boolean
  [SharedMemorySize](#cfn-ecs-taskdefinition-linuxparameters-sharedmemorysize): Integer
  [Tmpfs](#cfn-ecs-taskdefinition-linuxparameters-tmpfs): 
    - [Tmpfs](aws-properties-ecs-taskdefinition-tmpfs.md)
```

## Properties<a name="aws-properties-ecs-taskdefinition-linuxparameters-properties"></a>

`Capabilities`  <a name="cfn-ecs-taskdefinition-linuxparameters-capabilities"></a>
The Linux capabilities for the container that are added to or dropped from the default configuration provided by Docker\.  
If you are using tasks that use the Fargate launch type, `capabilities` is supported but the `add` parameter is not supported\.
*Required*: No  
*Type*: [KernelCapabilities](aws-properties-ecs-taskdefinition-kernelcapabilities.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Devices`  <a name="cfn-ecs-taskdefinition-linuxparameters-devices"></a>
Any host devices to expose to the container\. This parameter maps to `Devices` in the [Create a container](https://docs.docker.com/engine/api/v1.35/#operation/ContainerCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `--device` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
If you are using tasks that use the Fargate launch type, the `devices` parameter is not supported\.
*Required*: No  
*Type*: List of [Device](aws-properties-ecs-taskdefinition-device.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InitProcessEnabled`  <a name="cfn-ecs-taskdefinition-linuxparameters-initprocessenabled"></a>
Run an `init` process inside the container that forwards signals and reaps processes\. This parameter maps to the `--init` option to [docker run](https://docs.docker.com/engine/reference/run/)\. This parameter requires version 1\.25 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log in to your container instance and run the following command: `sudo docker version --format '{{.Server.APIVersion}}'`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SharedMemorySize`  <a name="cfn-ecs-taskdefinition-linuxparameters-sharedmemorysize"></a>
The value for the size \(in MiB\) of the `/dev/shm` volume\. This parameter maps to the `--shm-size` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
If you are using tasks that use the Fargate launch type, the `sharedMemorySize` parameter is not supported\.
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tmpfs`  <a name="cfn-ecs-taskdefinition-linuxparameters-tmpfs"></a>
The container path, mount options, and size \(in MiB\) of the tmpfs mount\. This parameter maps to the `--tmpfs` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
If you are using tasks that use the Fargate launch type, the `tmpfs` parameter is not supported\.
*Required*: No  
*Type*: [List](aws-properties-ecs-taskdefinition-tmpfs.md) of [Tmpfs](aws-properties-ecs-taskdefinition-tmpfs.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Supported Regions

This PropertyType is supported by ***all*** regions.