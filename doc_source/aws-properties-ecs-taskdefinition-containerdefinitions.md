# Amazon Elastic Container Service TaskDefinition ContainerDefinition<a name="aws-properties-ecs-taskdefinition-containerdefinitions"></a>

The `ContainerDefinition` property type describes the configuration of an Amazon Elastic Container Service \(Amazon ECS\) container\. The container definitions are passed to the Docker daemon\.

The `ContainerDefinitions` property of the [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md) resource contains a list of `ContainerDefinition` property types\.

## Syntax<a name="aws-properties-ecs-taskdefinition-containerdefinitions-syntax"></a>

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-syntax.json"></a>

```
{
  "[Command](#cfn-ecs-taskdefinition-containerdefinition-command)" : [ String, ... ],
  "[Cpu](#cfn-ecs-taskdefinition-containerdefinition-cpu)" : Integer,
  "[DisableNetworking](#cfn-ecs-taskdefinition-containerdefinition-disablenetworking)" : Boolean,
  "[DnsSearchDomains](#cfn-ecs-taskdefinition-containerdefinition-dnssearchdomains)" : [ String, ... ],
  "[DnsServers](#cfn-ecs-taskdefinition-containerdefinition-dnsservers)" : [ String, ... ],
  "[DockerLabels](#cfn-ecs-taskdefinition-containerdefinition-dockerlabels)" : { String:String, ... },
  "[DockerSecurityOptions](#cfn-ecs-taskdefinition-containerdefinition-dockersecurityoptions)" : [ String, ... ],
  "[EntryPoint](#cfn-ecs-taskdefinition-containerdefinition-entrypoint)" : [ String, ... ],
  "[Environment](#cfn-ecs-taskdefinition-containerdefinition-environment)" : [ [*KeyValuePair*](aws-properties-ecs-taskdefinition-containerdefinitions-environment.md), ... ],
  "[Essential](#cfn-ecs-taskdefinition-containerdefinition-essential)" : Boolean,
  "[ExtraHosts](#cfn-ecs-taskdefinition-containerdefinition-extrahosts)" : [ [*HostEntry*](aws-properties-ecs-taskdefinition-containerdefinitions-hostentry.md), ... ],
  "[HealthCheck](#cfn-ecs-taskdefinition-containerdefinition-healthcheck)" : [*HealthCheck*](aws-properties-ecs-taskdefinition-healthcheck.md),
  "[Hostname](#cfn-ecs-taskdefinition-containerdefinition-hostname)" : String,
  "[Image](#cfn-ecs-taskdefinition-containerdefinition-image)" : String,
  "[Links](#cfn-ecs-taskdefinition-containerdefinition-links)" : [ String, ... ],
  "[LinuxParameters](#cfn-ecs-taskdefinition-containerdefinition-linuxparameters)" : [*LinuxParameters*](aws-properties-ecs-taskdefinition-linuxparameters.md),
  "[LogConfiguration](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration)" : [*LogConfiguration*](aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration.md),
  "[Memory](#cfn-ecs-taskdefinition-containerdefinition-memory)" : Integer,
  "[MemoryReservation](#cfn-ecs-taskdefinition-containerdefinition-memoryreservation)" : Integer,
  "[MountPoints](#cfn-ecs-taskdefinition-containerdefinition-mountpoints)" : [ [*MountPoint*](aws-properties-ecs-taskdefinition-containerdefinitions-mountpoints.md), ... ],
  "[Name](#cfn-ecs-taskdefinition-containerdefinition-name)" : String,
  "[PortMappings](#cfn-ecs-taskdefinition-containerdefinition-portmappings)" : [ [*PortMapping*](aws-properties-ecs-taskdefinition-containerdefinitions-portmappings.md), ... ],
  "[Privileged](#cfn-ecs-taskdefinition-containerdefinition-privileged)" : Boolean,
  "[ReadonlyRootFilesystem](#cfn-ecs-taskdefinition-containerdefinition-readonlyrootfilesystem)" : Boolean,
  "[Ulimits](#cfn-ecs-taskdefinition-containerdefinition-ulimits)" : [ [*Ulimit*](aws-properties-ecs-taskdefinition-containerdefinitions-ulimit.md), ... ],
  "[User](#cfn-ecs-taskdefinition-containerdefinition-user)" : String,
  "[VolumesFrom](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom)" : [ [*VolumeFrom*](aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom.md), ... ],
  "[WorkingDirectory](#cfn-ecs-taskdefinition-containerdefinition-workingdirectory)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-syntax.yaml"></a>

```
[Command](#cfn-ecs-taskdefinition-containerdefinition-command):
  - String
[Cpu](#cfn-ecs-taskdefinition-containerdefinition-cpu): Integer
[DisableNetworking](#cfn-ecs-taskdefinition-containerdefinition-disablenetworking): Boolean
[DnsSearchDomains](#cfn-ecs-taskdefinition-containerdefinition-dnssearchdomains):
  - String
[DnsServers](#cfn-ecs-taskdefinition-containerdefinition-dnsservers):
  - String
[DockerLabels](#cfn-ecs-taskdefinition-containerdefinition-dockerlabels):
  String: String
[DockerSecurityOptions](#cfn-ecs-taskdefinition-containerdefinition-dockersecurityoptions):
  - String
[EntryPoint](#cfn-ecs-taskdefinition-containerdefinition-entrypoint):
  - String
[Environment](#cfn-ecs-taskdefinition-containerdefinition-environment):
  - [*KeyValuePair*](aws-properties-ecs-taskdefinition-containerdefinitions-environment.md)
[Essential](#cfn-ecs-taskdefinition-containerdefinition-essential): Boolean
[ExtraHosts](#cfn-ecs-taskdefinition-containerdefinition-extrahosts):
  - [*HostEntry*](aws-properties-ecs-taskdefinition-containerdefinitions-hostentry.md)
[HealthCheck](#cfn-ecs-taskdefinition-containerdefinition-healthcheck):
  [*HealthCheck*](aws-properties-ecs-taskdefinition-healthcheck.md)
[Hostname](#cfn-ecs-taskdefinition-containerdefinition-hostname): String
[Image](#cfn-ecs-taskdefinition-containerdefinition-image): String
[Links](#cfn-ecs-taskdefinition-containerdefinition-links):
  - String
[LinuxParameters](#cfn-ecs-taskdefinition-containerdefinition-linuxparameters): 
  [*LinuxParameters*](aws-properties-ecs-taskdefinition-linuxparameters.md)
[LogConfiguration](#cfn-ecs-taskdefinition-containerdefinition-logconfiguration):
  [*LogConfiguration*](aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration.md)
[Memory](#cfn-ecs-taskdefinition-containerdefinition-memory): Integer
[MemoryReservation](#cfn-ecs-taskdefinition-containerdefinition-memoryreservation): Integer
[MountPoints](#cfn-ecs-taskdefinition-containerdefinition-mountpoints):
  - [*MountPoint*](aws-properties-ecs-taskdefinition-containerdefinitions-mountpoints.md)
[Name](#cfn-ecs-taskdefinition-containerdefinition-name): String
[PortMappings](#cfn-ecs-taskdefinition-containerdefinition-portmappings):
  - [*PortMapping*](aws-properties-ecs-taskdefinition-containerdefinitions-portmappings.md)
[Privileged](#cfn-ecs-taskdefinition-containerdefinition-privileged): Boolean
[ReadonlyRootFilesystem](#cfn-ecs-taskdefinition-containerdefinition-readonlyrootfilesystem): Boolean
[Ulimits](#cfn-ecs-taskdefinition-containerdefinition-ulimits):
  - [*Ulimit*](aws-properties-ecs-taskdefinition-containerdefinitions-ulimit.md)
[User](#cfn-ecs-taskdefinition-containerdefinition-user): String
[VolumesFrom](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom):
  - [*VolumeFrom*](aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom.md)
[WorkingDirectory](#cfn-ecs-taskdefinition-containerdefinition-workingdirectory): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-containerdefinitions-properties"></a>

For more information about each property, see [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*\.

`Command`  <a name="cfn-ecs-taskdefinition-containerdefinition-command"></a>
The `CMD` value to pass to the container\. For more information about the Docker `CMD` parameter, see [https://docs\.docker\.com/engine/reference/builder/\#cmd](https://docs.docker.com/engine/reference/builder/#cmd)\.  
*Required*: No  
*Type*: List of String values

`Cpu`  <a name="cfn-ecs-taskdefinition-containerdefinition-cpu"></a>
The minimum number of CPU units to reserve for the container\. Containers share unallocated CPU units with other containers on the instance by using the same ratio as their allocated CPU units\. For more information, see the `cpu` content for the [ContainerDefinition](http://docs.aws.amazon.com/AmazonECS/latest/APIReference//API_ContainerDefinition.html) data type in the *Amazon Elastic Container Service API Reference*\.  
*Required*: No  
*Type*: Integer

`DisableNetworking`  <a name="cfn-ecs-taskdefinition-containerdefinition-disablenetworking"></a>
Indicates whether networking is disabled within the container\.  
*Required*: No  
*Type*: Boolean

`DnsSearchDomains`  <a name="cfn-ecs-taskdefinition-containerdefinition-dnssearchdomains"></a>
A list of DNS search domains that are provided to the container\. The domain names that the DNS logic looks up when a process attempts to access a bare unqualified hostname\.  
*Required*: No  
*Type*: List of String values

`DnsServers`  <a name="cfn-ecs-taskdefinition-containerdefinition-dnsservers"></a>
A list of DNS servers that Amazon ECS provides to the container\.  
*Required*: No  
*Type*: List of String values

`DockerLabels`  <a name="cfn-ecs-taskdefinition-containerdefinition-dockerlabels"></a>
A key\-value map of labels for the container\.  
*Required*: No  
*Type*: Key\-value pairs, with the name of the label as the key and the label value as the value\.

`DockerSecurityOptions`  <a name="cfn-ecs-taskdefinition-containerdefinition-dockersecurityoptions"></a>
A list of custom labels for SELinux and AppArmor multi\-level security systems\. For more information, see the `dockerSecurityOptions` content for the [ContainerDefinition](http://docs.aws.amazon.com/AmazonECS/latest/APIReference//API_ContainerDefinition.html) data type in the *Amazon Elastic Container Service API Reference*\.  
*Required*: No  
*Type*: List of String values

`EntryPoint`  <a name="cfn-ecs-taskdefinition-containerdefinition-entrypoint"></a>
The `ENTRYPOINT` value to pass to the container\. For more information about the Docker `ENTRYPOINT` parameter, see [https://docs\.docker\.com/engine/reference/builder/\#entrypoint](https://docs.docker.com/engine/reference/builder/#entrypoint)\.  
*Required*: No  
*Type*: List of String values

`Environment`  <a name="cfn-ecs-taskdefinition-containerdefinition-environment"></a>
The environment variables to pass to the container\.  
*Required*: No  
*Type*: List of [Amazon ECS TaskDefinition KeyValuePair](aws-properties-ecs-taskdefinition-containerdefinitions-environment.md) property types

`Essential`  <a name="cfn-ecs-taskdefinition-containerdefinition-essential"></a>
Indicates whether the task stops if this container fails\. If you specify **true** and the container fails, all other containers in the task stop\. If you specify **false** and the container fails, none of the other containers in the task is affected\. This value is **true** by default\.  
You must have at least one essential container in a task\.  
*Required*: No  
*Type*: Boolean

`ExtraHosts`  <a name="cfn-ecs-taskdefinition-containerdefinition-extrahosts"></a>
A list of hostnames and IP address mappings to append to the `/etc/hosts` file on the container\.  
*Required*: No  
*Type*: List of [Amazon ECS TaskDefinition HostEntry](aws-properties-ecs-taskdefinition-containerdefinitions-hostentry.md) property types

`HealthCheck`  <a name="cfn-ecs-taskdefinition-containerdefinition-healthcheck"></a>
A container health check\. Health check parameters that are specified in a container definition override any Docker health checks that exist in the container image \(such as those specified in a parent image or from the image's Dockerfile\)\.  
*Required*: No  
*Type*: [Amazon ECS TaskDefinition HealthCheckAmazon SageMaker Endpoint TagAmazon SageMaker EndpointConfig ProductionVariantAmazon SageMaker NotebookInstanceLifecycleConfig NotebookInstanceLifecycleHook](aws-properties-ecs-taskdefinition-healthcheck.md)

`Hostname`  <a name="cfn-ecs-taskdefinition-containerdefinition-hostname"></a>
The name that Docker uses for the container hostname\.  
*Required*: No  
*Type*: String

`Image`  <a name="cfn-ecs-taskdefinition-containerdefinition-image"></a>
The image to use for a container\. The image is passed directly to the Docker daemon\. You can use images in the Docker Hub registry or specify other repositories \(*repository\-url*/*image*:*tag*\)\.  
*Required*: Yes  
*Type*: String

`Links`  <a name="cfn-ecs-taskdefinition-containerdefinition-links"></a>
The name of another container to connect to\. With links, containers can communicate with each other without using port mappings\.  
*Required*: No  
*Type*: List of String values

`LinuxParameters`  <a name="cfn-ecs-taskdefinition-containerdefinition-linuxparameters"></a>
The Linux\-specific options that are applied to the container\.  
 *Required*: No  
 *Type*: [Amazon ECS TaskDefinition LinuxParameters](aws-properties-ecs-taskdefinition-linuxparameters.md)

`LogConfiguration`  <a name="cfn-ecs-taskdefinition-containerdefinition-logconfiguration"></a>
Configures a custom log driver for the container\. For more information, see the `logConfiguration` content for the [ContainerDefinition](http://docs.aws.amazon.com/AmazonECS/latest/APIReference//API_ContainerDefinition.html) data type in the *Amazon Elastic Container Service API Reference*\.  
*Required*: No  
*Type*: [Amazon ECS TaskDefinition LogConfiguration](aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration.md)

`Memory`  <a name="cfn-ecs-taskdefinition-containerdefinition-memory"></a>
The number of MiB of memory to reserve for the container\. If your container attempts to exceed the allocated memory, the container is terminated\.  
*Required*: Conditional\. You must specify one or both of the `Memory` or `MemoryReservation` properties\. If you specify both, the value for the `Memory` property must be greater than the value of the `MemoryReservation` property\.  
*Type*: Integer

`MemoryReservation`  <a name="cfn-ecs-taskdefinition-containerdefinition-memoryreservation"></a>
The number of MiB of memory to reserve for the container\. When system memory is under contention, Docker attempts to keep the container memory within the limit\. If the container requires more memory, it can consume up to the value specified by the `Memory` property or all of the available memory on the container instance—whichever comes first\. This is called a soft limit\.  
*Required*: Conditional\. You must specify one or both of the `Memory` or `MemoryReservation` properties\. If you specify both, the value for the `Memory` property must be greater than the value of the `MemoryReservation` property\.  
*Type*: Integer

`MountPoints`  <a name="cfn-ecs-taskdefinition-containerdefinition-mountpoints"></a>
The mount points for data volumes in the container\.  
*Required*: No  
*Type*: List of [Amazon ECS TaskDefinition MountPoint](aws-properties-ecs-taskdefinition-containerdefinitions-mountpoints.md) property types

`Name`  <a name="cfn-ecs-taskdefinition-containerdefinition-name"></a>
A name for the container\.  
*Required*: Yes  
*Type*: String

`PortMappings`  <a name="cfn-ecs-taskdefinition-containerdefinition-portmappings"></a>
A mapping of the container port to a host port\. Port mappings enable containers to access ports on the host container instance to send or receive traffic\.  
*Required*: No  
*Type*: List of [Amazon ECS TaskDefinition ContainerDefinitions PortMapping](aws-properties-ecs-taskdefinition-containerdefinitions-portmappings.md) property types

`Privileged`  <a name="cfn-ecs-taskdefinition-containerdefinition-privileged"></a>
Indicates whether the container is given full access to the host container instance\.  
*Required*: No  
*Type*: Boolean

`ReadonlyRootFilesystem`  <a name="cfn-ecs-taskdefinition-containerdefinition-readonlyrootfilesystem"></a>
Indicates whether the container's root file system is mounted as read only\.  
*Required*: No  
*Type*: Boolean

`Ulimits`  <a name="cfn-ecs-taskdefinition-containerdefinition-ulimits"></a>
A list of ulimits to set in the container\. The ulimits set constraints on how many resources a container can consume so that it doesn't deplete all available resources on the host\.  
*Required*: No  
*Type*: List of [Amazon ECS TaskDefinition Ulimit](aws-properties-ecs-taskdefinition-containerdefinitions-ulimit.md) property types

`User`  <a name="cfn-ecs-taskdefinition-containerdefinition-user"></a>
The user name to use inside the container\.  
*Required*: No  
*Type*: String

`VolumesFrom`  <a name="cfn-ecs-taskdefinition-containerdefinition-volumesfrom"></a>
The data volumes to mount from another container\.  
*Required*: No  
*Type*: List of [Amazon ECS TaskDefinition VolumeFrom](aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom.md) property types

`WorkingDirectory`  <a name="cfn-ecs-taskdefinition-containerdefinition-workingdirectory"></a>
The working directory in the container to run commands in\.  
*Required*: No  
*Type*: String

## See Also<a name="aws-properties-ecs-taskdefinition-containerdefinitions-seealso"></a>
+ [Task Definition Parameters](http://docs.aws.amazon.com/AmazonECS/latest/developerguide//task_definition_parameters.html) in the *Amazon Elastic Container Service Developer Guide*