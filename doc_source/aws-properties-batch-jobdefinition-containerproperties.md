# AWS::Batch::JobDefinition ContainerProperties<a name="aws-properties-batch-jobdefinition-containerproperties"></a>

Container properties are used in job definitions to describe the container that's launched as part of a job\.

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-syntax.json"></a>

```
{
  "[Command](#cfn-batch-jobdefinition-containerproperties-command)" : [ String, ... ],
  "[Environment](#cfn-batch-jobdefinition-containerproperties-environment)" : [ Environment, ... ],
  "[ExecutionRoleArn](#cfn-batch-jobdefinition-containerproperties-executionrolearn)" : String,
  "[FargatePlatformConfiguration](#cfn-batch-jobdefinition-containerproperties-fargateplatformconfiguration)" : FargatePlatformConfiguration,
  "[Image](#cfn-batch-jobdefinition-containerproperties-image)" : String,
  "[InstanceType](#cfn-batch-jobdefinition-containerproperties-instancetype)" : String,
  "[JobRoleArn](#cfn-batch-jobdefinition-containerproperties-jobrolearn)" : String,
  "[LinuxParameters](#cfn-batch-jobdefinition-containerproperties-linuxparameters)" : LinuxParameters,
  "[LogConfiguration](#cfn-batch-jobdefinition-containerproperties-logconfiguration)" : LogConfiguration,
  "[Memory](#cfn-batch-jobdefinition-containerproperties-memory)" : Integer,
  "[MountPoints](#cfn-batch-jobdefinition-containerproperties-mountpoints)" : [ MountPoints, ... ],
  "[NetworkConfiguration](#cfn-batch-jobdefinition-containerproperties-networkconfiguration)" : NetworkConfiguration,
  "[Privileged](#cfn-batch-jobdefinition-containerproperties-privileged)" : Boolean,
  "[ReadonlyRootFilesystem](#cfn-batch-jobdefinition-containerproperties-readonlyrootfilesystem)" : Boolean,
  "[ResourceRequirements](#cfn-batch-jobdefinition-containerproperties-resourcerequirements)" : [ ResourceRequirement, ... ],
  "[Secrets](#cfn-batch-jobdefinition-containerproperties-secrets)" : [ Secret, ... ],
  "[Ulimits](#cfn-batch-jobdefinition-containerproperties-ulimits)" : [ Ulimit, ... ],
  "[User](#cfn-batch-jobdefinition-containerproperties-user)" : String,
  "[Vcpus](#cfn-batch-jobdefinition-containerproperties-vcpus)" : Integer,
  "[Volumes](#cfn-batch-jobdefinition-containerproperties-volumes)" : [ Volumes, ... ]
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-syntax.yaml"></a>

```
  [Command](#cfn-batch-jobdefinition-containerproperties-command): 
    - String
  [Environment](#cfn-batch-jobdefinition-containerproperties-environment): 
    - Environment
  [ExecutionRoleArn](#cfn-batch-jobdefinition-containerproperties-executionrolearn): String
  [FargatePlatformConfiguration](#cfn-batch-jobdefinition-containerproperties-fargateplatformconfiguration): 
    FargatePlatformConfiguration
  [Image](#cfn-batch-jobdefinition-containerproperties-image): String
  [InstanceType](#cfn-batch-jobdefinition-containerproperties-instancetype): String
  [JobRoleArn](#cfn-batch-jobdefinition-containerproperties-jobrolearn): String
  [LinuxParameters](#cfn-batch-jobdefinition-containerproperties-linuxparameters): 
    LinuxParameters
  [LogConfiguration](#cfn-batch-jobdefinition-containerproperties-logconfiguration): 
    LogConfiguration
  [Memory](#cfn-batch-jobdefinition-containerproperties-memory): Integer
  [MountPoints](#cfn-batch-jobdefinition-containerproperties-mountpoints): 
    - MountPoints
  [NetworkConfiguration](#cfn-batch-jobdefinition-containerproperties-networkconfiguration): 
    NetworkConfiguration
  [Privileged](#cfn-batch-jobdefinition-containerproperties-privileged): Boolean
  [ReadonlyRootFilesystem](#cfn-batch-jobdefinition-containerproperties-readonlyrootfilesystem): Boolean
  [ResourceRequirements](#cfn-batch-jobdefinition-containerproperties-resourcerequirements): 
    - ResourceRequirement
  [Secrets](#cfn-batch-jobdefinition-containerproperties-secrets): 
    - Secret
  [Ulimits](#cfn-batch-jobdefinition-containerproperties-ulimits): 
    - Ulimit
  [User](#cfn-batch-jobdefinition-containerproperties-user): String
  [Vcpus](#cfn-batch-jobdefinition-containerproperties-vcpus): Integer
  [Volumes](#cfn-batch-jobdefinition-containerproperties-volumes): 
    - Volumes
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-properties"></a>

`Command`  <a name="cfn-batch-jobdefinition-containerproperties-command"></a>
The command that's passed to the container\. This parameter maps to `Cmd` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `COMMAND` parameter to [docker run](https://docs.docker.com/engine/reference/run/)\. For more information, see [https://docs\.docker\.com/engine/reference/builder/\#cmd](https://docs.docker.com/engine/reference/builder/#cmd)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Environment`  <a name="cfn-batch-jobdefinition-containerproperties-environment"></a>
The environment variables to pass to a container\. This parameter maps to `Env` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--env` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
We don't recommend using plaintext environment variables for sensitive information, such as credential data\.
Environment variables must not start with `AWS_BATCH`; this naming convention is reserved for variables that are set by the AWS Batch service\.
*Required*: No  
*Type*: [List](aws-properties-batch-jobdefinition-environment.md) of [Environment](aws-properties-batch-jobdefinition-environment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionRoleArn`  <a name="cfn-batch-jobdefinition-containerproperties-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the execution role that AWS Batch can assume\. Jobs running on Fargate resources must provide an execution role\. For more information, see [AWS Batch execution IAM role](https://docs.aws.amazon.com/batch/latest/userguide/execution-IAM-role.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FargatePlatformConfiguration`  <a name="cfn-batch-jobdefinition-containerproperties-fargateplatformconfiguration"></a>
The platform configuration for jobs running on Fargate resources\. Jobs running on EC2 resources must not specify this parameter\.  
*Required*: No  
*Type*: [FargatePlatformConfiguration](aws-properties-batch-jobdefinition-containerproperties-fargateplatformconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Image`  <a name="cfn-batch-jobdefinition-containerproperties-image"></a>
The image used to start a container\. This string is passed directly to the Docker daemon\. Images in the Docker Hub registry are available by default\. Other repositories are specified with ` repository-url/image:tag `\. Up to 255 letters \(uppercase and lowercase\), numbers, hyphens, underscores, colons, periods, forward slashes, and number signs are allowed\. This parameter maps to `Image` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `IMAGE` parameter of [docker run](https://docs.docker.com/engine/reference/run/)\.  
Docker image architecture must match the processor architecture of the compute resources that they're scheduled on\. For example, ARM\-based Docker images can only run on ARM\-based compute resources\.
+ Images in Amazon ECR repositories use the full registry and repository URI \(for example, `012345678910.dkr.ecr.<region-name>.amazonaws.com/<repository-name>`\)\.
+ Images in official repositories on Docker Hub use a single name \(for example, `ubuntu` or `mongo`\)\.
+ Images in other repositories on Docker Hub are qualified with an organization name \(for example, `amazon/amazon-ecs-agent`\)\.
+ Images in other online repositories are qualified further by a domain name \(for example, `quay.io/assemblyline/ubuntu`\)\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-batch-jobdefinition-containerproperties-instancetype"></a>
The instance type to use for a multi\-node parallel job\. All node groups in a multi\-node parallel job must use the same instance type\.  
This parameter isn't applicable to single\-node container jobs or for jobs running on Fargate resources and shouldn't be provided\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobRoleArn`  <a name="cfn-batch-jobdefinition-containerproperties-jobrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that the container can assume for AWS permissions\. For more information, see [IAM Roles for Tasks](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-iam-roles.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LinuxParameters`  <a name="cfn-batch-jobdefinition-containerproperties-linuxparameters"></a>
Linux\-specific modifications that are applied to the container, such as details for device mappings\.  
*Required*: No  
*Type*: [LinuxParameters](aws-properties-batch-jobdefinition-containerproperties-linuxparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogConfiguration`  <a name="cfn-batch-jobdefinition-containerproperties-logconfiguration"></a>
The log configuration specification for the container\.  
This parameter maps to `LogConfig` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--log-driver` option to [docker run](https://docs.docker.com/engine/reference/run/)\. By default, containers use the same logging driver that the Docker daemon uses\. However the container might use a different logging driver than the Docker daemon by specifying a log driver with this parameter in the container definition\. To use a different logging driver for a container, the log system must be configured properly on the container instance \(or on a different log server for remote logging options\)\. For more information on the options for different supported log drivers, see [Configure logging drivers](https://docs.docker.com/engine/admin/logging/overview/) in the Docker documentation\.  
AWS Batch currently supports a subset of the logging drivers available to the Docker daemon \(shown in the [LogConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties.html#cfn-batch-jobdefinition-containerproperties-logconfiguration) data type\)\.
This parameter requires version 1\.18 of the Docker Remote API or greater on your container instance\. To check the Docker Remote API version on your container instance, log into your container instance and run the following command: `sudo docker version | grep "Server API version"`   
The Amazon ECS container agent running on a container instance must register the logging drivers available on that instance with the `ECS_AVAILABLE_LOGGING_DRIVERS` environment variable before containers placed on that instance can use these log configuration options\. For more information, see [Amazon ECS Container Agent Configuration](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-agent-config.html) in the *Amazon Elastic Container Service Developer Guide*\.
*Required*: No  
*Type*: [LogConfiguration](aws-properties-batch-jobdefinition-containerproperties-logconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Memory`  <a name="cfn-batch-jobdefinition-containerproperties-memory"></a>
This parameter is deprecated and not supported for jobs run on Fargate resources, use `ResourceRequirement`\. For jobs run on EC2 resources can specify the memory requirement using the `ResourceRequirement` structure\. The hard limit \(in MiB\) of memory to present to the container\. If your container attempts to exceed the memory specified here, the container is killed\. This parameter maps to `Memory` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--memory` option to [docker run](https://docs.docker.com/engine/reference/run/)\. You must specify at least 4 MiB of memory for a job\. This is required but can be specified in several places; it must be specified for each node at least once\.  
If you're trying to maximize your resource utilization by providing your jobs as much memory as possible for a particular instance type, see [Memory Management](https://docs.aws.amazon.com/batch/latest/userguide/memory-management.html) in the *AWS Batch User Guide*\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MountPoints`  <a name="cfn-batch-jobdefinition-containerproperties-mountpoints"></a>
The mount points for data volumes in your container\. This parameter maps to `Volumes` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--volume` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
*Required*: No  
*Type*: [List](aws-properties-batch-jobdefinition-mountpoints.md) of [MountPoints](aws-properties-batch-jobdefinition-mountpoints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkConfiguration`  <a name="cfn-batch-jobdefinition-containerproperties-networkconfiguration"></a>
The network configuration for jobs running on Fargate resources\. Jobs running on EC2 resources must not specify this parameter\.  
*Required*: No  
*Type*: [NetworkConfiguration](aws-properties-batch-jobdefinition-containerproperties-networkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Privileged`  <a name="cfn-batch-jobdefinition-containerproperties-privileged"></a>
When this parameter is true, the container is given elevated permissions on the host container instance \(similar to the `root` user\)\. This parameter maps to `Privileged` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--privileged` option to [docker run](https://docs.docker.com/engine/reference/run/)\. The default value is false\.  
This parameter isn't applicable to jobs running on Fargate resources and shouldn't be provided, or specified as false\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadonlyRootFilesystem`  <a name="cfn-batch-jobdefinition-containerproperties-readonlyrootfilesystem"></a>
When this parameter is true, the container is given read\-only access to its root file system\. This parameter maps to `ReadonlyRootfs` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--read-only` option to `docker run`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceRequirements`  <a name="cfn-batch-jobdefinition-containerproperties-resourcerequirements"></a>
The type and amount of resources to assign to a container\. The supported resources include `GPU`, `MEMORY`, and `VCPU`\.  
*Required*: No  
*Type*: List of [ResourceRequirement](aws-properties-batch-jobdefinition-resourcerequirement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Secrets`  <a name="cfn-batch-jobdefinition-containerproperties-secrets"></a>
The secrets for the container\. For more information, see [Specifying sensitive data](https://docs.aws.amazon.com/batch/latest/userguide/specifying-sensitive-data.html) in the *AWS Batch User Guide*\.  
*Required*: No  
*Type*: List of [Secret](aws-properties-batch-jobdefinition-secret.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ulimits`  <a name="cfn-batch-jobdefinition-containerproperties-ulimits"></a>
A list of `ulimits` to set in the container\. This parameter maps to `Ulimits` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--ulimit` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
This parameter isn't applicable to jobs running on Fargate resources and shouldn't be provided\.
*Required*: No  
*Type*: List of [Ulimit](aws-properties-batch-jobdefinition-ulimit.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`User`  <a name="cfn-batch-jobdefinition-containerproperties-user"></a>
The user name to use inside the container\. This parameter maps to `User` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--user` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Vcpus`  <a name="cfn-batch-jobdefinition-containerproperties-vcpus"></a>
This parameter is deprecated and not supported for jobs run on Fargate resources, see `resourceRequirement`\. The number of vCPUs reserved for the container\. Jobs running on EC2 resources can specify the vCPU requirement for the job using `resourceRequirements` but the vCPU requirements can't be specified both here and in the `resourceRequirement` structure\. This parameter maps to `CpuShares` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--cpu-shares` option to [docker run](https://docs.docker.com/engine/reference/run/)\. Each vCPU is equivalent to 1,024 CPU shares\. You must specify at least one vCPU\. This is required but can be specified in several places\. It must be specified for each node at least once\.  
This parameter isn't applicable to jobs running on Fargate resources and shouldn't be provided\. Jobs running on Fargate resources must specify the vCPU requirement for the job using `resourceRequirements`\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Volumes`  <a name="cfn-batch-jobdefinition-containerproperties-volumes"></a>
A list of data volumes used in a job\.  
*Required*: No  
*Type*: [List](aws-properties-batch-jobdefinition-volumes.md) of [Volumes](aws-properties-batch-jobdefinition-volumes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)