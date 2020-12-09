# AWS::ECS::TaskDefinition KernelCapabilities<a name="aws-properties-ecs-taskdefinition-kernelcapabilities"></a>

The `KernelCapabilities` property specifies the Linux capabilities for the container that are added to or dropped from the default configuration that is provided by Docker\. For more information on the default capabilities and the non\-default available capabilities, see [Runtime privilege and Linux capabilities](https://docs.docker.com/engine/reference/run/#runtime-privilege-and-linux-capabilities) in the *Docker run reference*\. For more detailed information on these Linux capabilities, see the [capabilities\(7\)](http://man7.org/linux/man-pages/man7/capabilities.7.html) Linux manual page\.

## Syntax<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-syntax.json"></a>

```
{
  "[Add](#cfn-ecs-taskdefinition-kernelcapabilities-add)" : [ String, ... ],
  "[Drop](#cfn-ecs-taskdefinition-kernelcapabilities-drop)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-syntax.yaml"></a>

```
  [Add](#cfn-ecs-taskdefinition-kernelcapabilities-add): 
    - String
  [Drop](#cfn-ecs-taskdefinition-kernelcapabilities-drop): 
    - String
```

## Properties<a name="aws-properties-ecs-taskdefinition-kernelcapabilities-properties"></a>

`Add`  <a name="cfn-ecs-taskdefinition-kernelcapabilities-add"></a>
The Linux capabilities for the container that have been added to the default configuration provided by Docker\. This parameter maps to `CapAdd` in the [Create a container](https://docs.docker.com/engine/api/v1.35/#operation/ContainerCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `--cap-add` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration)\.  
Tasks launched on AWS Fargate only support adding the `SYS_PTRACE` kernel capability\.
Valid values: `"ALL" | "AUDIT_CONTROL" | "AUDIT_WRITE" | "BLOCK_SUSPEND" | "CHOWN" | "DAC_OVERRIDE" | "DAC_READ_SEARCH" | "FOWNER" | "FSETID" | "IPC_LOCK" | "IPC_OWNER" | "KILL" | "LEASE" | "LINUX_IMMUTABLE" | "MAC_ADMIN" | "MAC_OVERRIDE" | "MKNOD" | "NET_ADMIN" | "NET_BIND_SERVICE" | "NET_BROADCAST" | "NET_RAW" | "SETFCAP" | "SETGID" | "SETPCAP" | "SETUID" | "SYS_ADMIN" | "SYS_BOOT" | "SYS_CHROOT" | "SYS_MODULE" | "SYS_NICE" | "SYS_PACCT" | "SYS_PTRACE" | "SYS_RAWIO" | "SYS_RESOURCE" | "SYS_TIME" | "SYS_TTY_CONFIG" | "SYSLOG" | "WAKE_ALARM"`   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Drop`  <a name="cfn-ecs-taskdefinition-kernelcapabilities-drop"></a>
The Linux capabilities for the container that have been removed from the default configuration provided by Docker\. This parameter maps to `CapDrop` in the [Create a container](https://docs.docker.com/engine/api/v1.35/#operation/ContainerCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `--cap-drop` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration)\.  
Valid values: `"ALL" | "AUDIT_CONTROL" | "AUDIT_WRITE" | "BLOCK_SUSPEND" | "CHOWN" | "DAC_OVERRIDE" | "DAC_READ_SEARCH" | "FOWNER" | "FSETID" | "IPC_LOCK" | "IPC_OWNER" | "KILL" | "LEASE" | "LINUX_IMMUTABLE" | "MAC_ADMIN" | "MAC_OVERRIDE" | "MKNOD" | "NET_ADMIN" | "NET_BIND_SERVICE" | "NET_BROADCAST" | "NET_RAW" | "SETFCAP" | "SETGID" | "SETPCAP" | "SETUID" | "SYS_ADMIN" | "SYS_BOOT" | "SYS_CHROOT" | "SYS_MODULE" | "SYS_NICE" | "SYS_PACCT" | "SYS_PTRACE" | "SYS_RAWIO" | "SYS_RESOURCE" | "SYS_TIME" | "SYS_TTY_CONFIG" | "SYSLOG" | "WAKE_ALARM"`   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)