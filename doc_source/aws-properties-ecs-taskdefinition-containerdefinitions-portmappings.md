# AWS::ECS::TaskDefinition PortMapping<a name="aws-properties-ecs-taskdefinition-containerdefinitions-portmappings"></a>

The `PortMapping` property specifies a port mapping\. Port mappings allow containers to access ports on the host container instance to send or receive traffic\. Port mappings are specified as part of the container definition\.

If you are using containers in a task with the `awsvpc` or `host` network mode, exposed ports should be specified using `containerPort`\. The `hostPort` can be left blank or it must be the same value as the `containerPort`\.

After a task reaches the `RUNNING` status, manual and automatic host and container port assignments are visible in the `networkBindings` section of [DescribeTasks](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DescribeTasks.html) API responses\.

## Syntax<a name="aws-properties-ecs-taskdefinition-containerdefinitions-portmappings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-portmappings-syntax.json"></a>

```
{
  "[ContainerPort](#cfn-ecs-taskdefinition-containerdefinition-portmappings-containerport)" : Integer,
  "[HostPort](#cfn-ecs-taskdefinition-containerdefinition-portmappings-readonly)" : Integer,
  "[Protocol](#cfn-ecs-taskdefinition-containerdefinition-portmappings-sourcevolume)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-portmappings-syntax.yaml"></a>

```
  [ContainerPort](#cfn-ecs-taskdefinition-containerdefinition-portmappings-containerport): Integer
  [HostPort](#cfn-ecs-taskdefinition-containerdefinition-portmappings-readonly): Integer
  [Protocol](#cfn-ecs-taskdefinition-containerdefinition-portmappings-sourcevolume): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-containerdefinitions-portmappings-properties"></a>

`ContainerPort`  <a name="cfn-ecs-taskdefinition-containerdefinition-portmappings-containerport"></a>
The port number on the container that is bound to the user\-specified or automatically assigned host port\.  
If you are using containers in a task with the `awsvpc` or `host` network mode, exposed ports should be specified using `containerPort`\.  
If you are using containers in a task with the `bridge` network mode and you specify a container port and not a host port, your container automatically receives a host port in the ephemeral port range\. For more information, see `hostPort`\. Port mappings that are automatically assigned in this way do not count toward the 100 reserved ports limit of a container instance\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostPort`  <a name="cfn-ecs-taskdefinition-containerdefinition-portmappings-readonly"></a>
The port number on the container instance to reserve for your container\.  
If you are using containers in a task with the `awsvpc` or `host` network mode, the `hostPort` can either be left blank or set to the same value as the `containerPort`\.  
If you are using containers in a task with the `bridge` network mode, you can specify a non\-reserved host port for your container port mapping, or you can omit the `hostPort` \(or set it to `0`\) while specifying a `containerPort` and your container automatically receives a port in the ephemeral port range for your container instance operating system and Docker version\.  
The default ephemeral port range for Docker version 1\.6\.0 and later is listed on the instance under `/proc/sys/net/ipv4/ip_local_port_range`\. If this kernel parameter is unavailable, the default ephemeral port range from 49153 through 65535 is used\. Do not attempt to specify a host port in the ephemeral port range as these are reserved for automatic assignment\. In general, ports below 32768 are outside of the ephemeral port range\.  
The default ephemeral port range from 49153 through 65535 is always used for Docker versions before 1\.6\.0\.
The default reserved ports are 22 for SSH, the Docker ports 2375 and 2376, and the Amazon ECS container agent ports 51678\-51680\. Any host port that was previously specified in a running task is also reserved while the task is running \(after a task stops, the host port is released\)\. The current reserved ports are displayed in the `remainingResources` of [DescribeContainerInstances](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DescribeContainerInstances.html) output\. A container instance can have up to 100 reserved ports at a time, including the default reserved ports\. Automatically assigned ports don't count toward the 100 reserved ports limit\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-ecs-taskdefinition-containerdefinition-portmappings-sourcevolume"></a>
The protocol used for the port mapping\. Valid values are `tcp` and `udp`\. The default is `tcp`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `tcp | udp`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)