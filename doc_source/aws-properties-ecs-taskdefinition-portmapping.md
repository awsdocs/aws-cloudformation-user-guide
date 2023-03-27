# AWS::ECS::TaskDefinition PortMapping<a name="aws-properties-ecs-taskdefinition-portmapping"></a>

The `PortMapping` property specifies a port mapping\. Port mappings allow containers to access ports on the host container instance to send or receive traffic\. Port mappings are specified as part of the container definition\.

If you are using containers in a task with the `awsvpc` or `host` network mode, exposed ports should be specified using `containerPort`\. The `hostPort` can be left blank or it must be the same value as the `containerPort`\.

After a task reaches the `RUNNING` status, manual and automatic host and container port assignments are visible in the `networkBindings` section of [DescribeTasks](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DescribeTasks.html) API responses\.

## Syntax<a name="aws-properties-ecs-taskdefinition-portmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-portmapping-syntax.json"></a>

```
{
  "[AppProtocol](#cfn-ecs-taskdefinition-portmapping-appprotocol)" : String,
  "[ContainerPort](#cfn-ecs-taskdefinition-portmapping-containerport)" : Integer,
  "[ContainerPortRange](#cfn-ecs-taskdefinition-portmapping-containerportrange)" : String,
  "[HostPort](#cfn-ecs-taskdefinition-portmapping-hostport)" : Integer,
  "[Name](#cfn-ecs-taskdefinition-portmapping-name)" : String,
  "[Protocol](#cfn-ecs-taskdefinition-portmapping-protocol)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-portmapping-syntax.yaml"></a>

```
  [AppProtocol](#cfn-ecs-taskdefinition-portmapping-appprotocol): String
  [ContainerPort](#cfn-ecs-taskdefinition-portmapping-containerport): Integer
  [ContainerPortRange](#cfn-ecs-taskdefinition-portmapping-containerportrange): String
  [HostPort](#cfn-ecs-taskdefinition-portmapping-hostport): Integer
  [Name](#cfn-ecs-taskdefinition-portmapping-name): String
  [Protocol](#cfn-ecs-taskdefinition-portmapping-protocol): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-portmapping-properties"></a>

`AppProtocol`  <a name="cfn-ecs-taskdefinition-portmapping-appprotocol"></a>
The application protocol that's used for the port mapping\. This parameter only applies to Service Connect\. We recommend that you set this parameter to be consistent with the protocol that your application uses\. If you set this parameter, Amazon ECS adds protocol\-specific connection handling to the Service Connect proxy\. If you set this parameter, Amazon ECS adds protocol\-specific telemetry in the Amazon ECS console and CloudWatch\.  
If you don't set a value for this parameter, then TCP is used\. However, Amazon ECS doesn't add protocol\-specific telemetry for TCP\.  
Tasks that run in a namespace can use short names to connect to services in the namespace\. Tasks can connect to services across all of the clusters in the namespace\. Tasks connect through a managed proxy container that collects logs and metrics for increased visibility\. Only the tasks that Amazon ECS services create are supported with Service Connect\. For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `grpc | http | http2`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContainerPort`  <a name="cfn-ecs-taskdefinition-portmapping-containerport"></a>
The port number on the container that's bound to the user\-specified or automatically assigned host port\.  
If you use containers in a task with the `awsvpc` or `host` network mode, specify the exposed ports using `containerPort`\.  
If you use containers in a task with the `bridge` network mode and you specify a container port and not a host port, your container automatically receives a host port in the ephemeral port range\. For more information, see `hostPort`\. Port mappings that are automatically assigned in this way do not count toward the 100 reserved ports limit of a container instance\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContainerPortRange`  <a name="cfn-ecs-taskdefinition-portmapping-containerportrange"></a>
The port number range on the container that's bound to the dynamically mapped host port range\.   
The following rules apply when you specify a `containerPortRange`:  
+ You must use either the `bridge` network mode or the `awsvpc` network mode\.
+ This parameter is available for both the EC2 and AWS Fargate launch types\.
+ This parameter is available for both the Linux and Windows operating systems\.
+ The container instance must have at least version 1\.67\.0 of the container agent and at least version 1\.67\.0\-1 of the `ecs-init` package 
+ You can specify a maximum of 100 port ranges per container\.
+ You do not specify a `hostPortRange`\. The value of the `hostPortRange` is set as follows:
  + For containers in a task with the `awsvpc` network mode, the `hostPort` is set to the same value as the `containerPort`\. This is a static mapping strategy\.
  + For containers in a task with the `bridge` network mode, the Amazon ECS agent finds open host ports from the default ephemeral range and passes it to docker to bind them to the container ports\.
+ The `containerPortRange` valid values are between 1 and 65535\.
+ A port can only be included in one port mapping per container\.
+ You cannot specify overlapping port ranges\.
+ The first port in the range must be less than last port in the range\.
+ Docker recommends that you turn off the docker\-proxy in the Docker daemon config file when you have a large number of ports\.

  For more information, see [ Issue \#11185](https://github.com/moby/moby/issues/11185) on the Github website\.

  For information about how to turn off the docker\-proxy in the Docker daemon config file, see [Docker daemon](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/bootstrap_container_instance.html#bootstrap_docker_daemon) in the *Amazon ECS Developer Guide*\.
You can call [https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DescribeTasks.html](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DescribeTasks.html) to view the `hostPortRange` which are the host ports that are bound to the container ports\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HostPort`  <a name="cfn-ecs-taskdefinition-portmapping-hostport"></a>
The port number on the container instance to reserve for your container\.  
If you are using containers in a task with the `awsvpc` or `host` network mode, the `hostPort` can either be left blank or set to the same value as the `containerPort`\.  
If you are using containers in a task with the `bridge` network mode, you can specify a non\-reserved host port for your container port mapping, or you can omit the `hostPort` \(or set it to `0`\) while specifying a `containerPort` and your container automatically receives a port in the ephemeral port range for your container instance operating system and Docker version\.  
The default ephemeral port range for Docker version 1\.6\.0 and later is listed on the instance under `/proc/sys/net/ipv4/ip_local_port_range`\. If this kernel parameter is unavailable, the default ephemeral port range from 49153 through 65535 is used\. Do not attempt to specify a host port in the ephemeral port range as these are reserved for automatic assignment\. In general, ports below 32768 are outside of the ephemeral port range\.  
The default ephemeral port range from 49153 through 65535 is always used for Docker versions before 1\.6\.0\.
The default reserved ports are 22 for SSH, the Docker ports 2375 and 2376, and the Amazon ECS container agent ports 51678\-51680\. Any host port that was previously specified in a running task is also reserved while the task is running \(after a task stops, the host port is released\)\. The current reserved ports are displayed in the `remainingResources` of [DescribeContainerInstances](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DescribeContainerInstances.html) output\. A container instance can have up to 100 reserved ports at a time, including the default reserved ports\. Automatically assigned ports don't count toward the 100 reserved ports limit\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-ecs-taskdefinition-portmapping-name"></a>
The name that's used for the port mapping\. This parameter only applies to Service Connect\. This parameter is the name that you use in the `serviceConnectConfiguration` of a service\. The name can include up to 64 characters\. The characters can include lowercase letters, numbers, underscores \(\_\), and hyphens \(\-\)\. The name can't start with a hyphen\.  
For more information, see [Service Connect](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-connect.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-ecs-taskdefinition-portmapping-protocol"></a>
The protocol used for the port mapping\. Valid values are `tcp` and `udp`\. The default is `tcp`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `tcp | udp`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)