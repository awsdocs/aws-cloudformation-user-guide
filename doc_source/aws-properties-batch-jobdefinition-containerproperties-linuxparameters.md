# AWS::Batch::JobDefinition LinuxParameters<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters"></a>

Linux\-specific modifications that are applied to the container, such as details for device mappings\.

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters-syntax.json"></a>

```
{
  "[Devices](#cfn-batch-jobdefinition-containerproperties-linuxparameters-devices)" : [ Device, ... ],
  "[InitProcessEnabled](#cfn-batch-jobdefinition-containerproperties-linuxparameters-initprocessenabled)" : Boolean,
  "[MaxSwap](#cfn-batch-jobdefinition-containerproperties-linuxparameters-maxswap)" : Integer,
  "[SharedMemorySize](#cfn-batch-jobdefinition-containerproperties-linuxparameters-sharedmemorysize)" : Integer,
  "[Swappiness](#cfn-batch-jobdefinition-containerproperties-linuxparameters-swappiness)" : Integer,
  "[Tmpfs](#cfn-batch-jobdefinition-containerproperties-linuxparameters-tmpfs)" : [ Tmpfs, ... ]
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters-syntax.yaml"></a>

```
  [Devices](#cfn-batch-jobdefinition-containerproperties-linuxparameters-devices): 
    - Device
  [InitProcessEnabled](#cfn-batch-jobdefinition-containerproperties-linuxparameters-initprocessenabled): Boolean
  [MaxSwap](#cfn-batch-jobdefinition-containerproperties-linuxparameters-maxswap): Integer
  [SharedMemorySize](#cfn-batch-jobdefinition-containerproperties-linuxparameters-sharedmemorysize): Integer
  [Swappiness](#cfn-batch-jobdefinition-containerproperties-linuxparameters-swappiness): Integer
  [Tmpfs](#cfn-batch-jobdefinition-containerproperties-linuxparameters-tmpfs): 
    - Tmpfs
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters-properties"></a>

`Devices`  <a name="cfn-batch-jobdefinition-containerproperties-linuxparameters-devices"></a>
Any host devices to expose to the container\. This parameter maps to `Devices` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--device` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
This parameter isn't applicable to jobs running on Fargate resources and shouldn't be provided\.
*Required*: No  
*Type*: List of [Device](aws-properties-batch-jobdefinition-device.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InitProcessEnabled`  <a name="cfn-batch-jobdefinition-containerproperties-linuxparameters-initprocessenabled"></a>
If true, run an `init` process inside the container that forwards signals and reaps processes\. This parameter maps to the `--init` option to [docker run](https://docs.docker.com/engine/reference/run/)\. This parameter requires version 1\.25 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log into your container instance and run the following command: `sudo docker version | grep "Server API version"`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSwap`  <a name="cfn-batch-jobdefinition-containerproperties-linuxparameters-maxswap"></a>
The total amount of swap memory \(in MiB\) a container can use\. This parameter is translated to the `--memory-swap` option to [docker run](https://docs.docker.com/engine/reference/run/) where the value is the sum of the container memory plus the `maxSwap` value\. For more information, see [ `--memory-swap` details](https://docs.docker.com/config/containers/resource_constraints/#--memory-swap-details) in the Docker documentation\.  
If a `maxSwap` value of `0` is specified, the container doesn't use swap\. Accepted values are `0` or any positive integer\. If the `maxSwap` parameter is omitted, the container doesn't use the swap configuration for the container instance it is running on\. A `maxSwap` value must be set for the `swappiness` parameter to be used\.  
This parameter isn't applicable to jobs running on Fargate resources and shouldn't be provided\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SharedMemorySize`  <a name="cfn-batch-jobdefinition-containerproperties-linuxparameters-sharedmemorysize"></a>
The value for the size \(in MiB\) of the `/dev/shm` volume\. This parameter maps to the `--shm-size` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
This parameter isn't applicable to jobs running on Fargate resources and shouldn't be provided\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Swappiness`  <a name="cfn-batch-jobdefinition-containerproperties-linuxparameters-swappiness"></a>
This allows you to tune a container's memory swappiness behavior\. A `swappiness` value of `0` causes swapping not to happen unless absolutely necessary\. A `swappiness` value of `100` causes pages to be swapped very aggressively\. Accepted values are whole numbers between `0` and `100`\. If the `swappiness` parameter isn't specified, a default value of `60` is used\. If a value isn't specified for `maxSwap` then this parameter is ignored\. If `maxSwap` is set to 0, the container doesn't use swap\. This parameter maps to the `--memory-swappiness` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
Consider the following when you use a per\-container swap configuration\.  
+ Swap space must be enabled and allocated on the container instance for the containers to use\.
**Note**  
The Amazon ECS optimized AMIs don't have swap enabled by default\. You must enable swap on the instance to use this feature\. For more information, see [Instance Store Swap Volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-store-swap-volumes.html) in the *Amazon EC2 User Guide for Linux Instances* or [How do I allocate memory to work as swap space in an Amazon EC2 instance by using a swap file?](http://aws.amazon.com/premiumsupport/knowledge-center/ec2-memory-swap-file/) 
+ The swap space parameters are only supported for job definitions using EC2 resources\.
+ If the `maxSwap` and `swappiness` parameters are omitted from a job definition, each container will have a default `swappiness` value of 60 and the total swap usage will be limited to two times the memory reservation of the container\.
This parameter isn't applicable to jobs running on Fargate resources and shouldn't be provided\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tmpfs`  <a name="cfn-batch-jobdefinition-containerproperties-linuxparameters-tmpfs"></a>
The container path, mount options, and size \(in MiB\) of the tmpfs mount\. This parameter maps to the `--tmpfs` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
This parameter isn't applicable to jobs running on Fargate resources and shouldn't be provided\.
*Required*: No  
*Type*: [List](aws-properties-batch-jobdefinition-tmpfs.md) of [Tmpfs](aws-properties-batch-jobdefinition-tmpfs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)