# AWS Batch JobDefinition ContainerProperties<a name="aws-properties-batch-jobdefinition-containerproperties"></a>

The `ContainerProperties` property type specifies various properties specific to container\-based jobs\.

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-mountpoints)" : [ MountPoints, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-user)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-volumes)" : [ Volumes, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-command)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-memory)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-privileged)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-environment)" : [ Environment, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-jobrolearn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-readonlyrootfilesystem)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-ulimits)" : [ Ulimit, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-vcpus)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-image)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-mountpoints): 
  - MountPoints
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-user): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-volumes): 
  - Volumes
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-command): 
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-memory): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-privileged): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-environment): 
  - Environment
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-jobrolearn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-readonlyrootfilesystem): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-ulimits): 
  - Ulimit
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-vcpus): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-batch-jobdefinition-containerproperties-image): String
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-properties"></a>

`MountPoints`  
The mount points for data volumes in your container\. This parameter maps to `Volumes` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--volume` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
 *Required*: no  
 *Type*: List of [AWS Batch JobDefinition MountPoints](aws-properties-batch-jobdefinition-mountpoints.md)  
 *Update requires*: No Interruption 

`User`  
The user name to use inside the container\. This parameter maps to `User` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--user` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
 *Required*: no  
*Type*: String  
 *Update requires*: No Interruption 

`Volumes`  
A list of data volumes used in a job\.  
 *Required*: no  
 *Type*: List of [AWS Batch JobDefinition Volumes](aws-properties-batch-jobdefinition-volumes.md)  
 *Update requires*: No Interruption 

`Command`  
The command that is passed to the container\. This parameter maps to `Cmd` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `COMMAND` parameter to [docker run](https://docs.docker.com/engine/reference/run/)\.  
 *Required*: no  
*Type*: List of String values  
 *Update requires*: No Interruption 

`Memory`  
The hard limit \(in MiB\) of memory to present to the container\. If your container attempts to exceed the memory specified here, the container is killed\. This parameter maps to `Memory` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--memory` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
 *Required*: yes  
*Type*: Integer  
 *Update requires*: No Interruption 

`Privileged`  
When this parameter is true, the container is given elevated privileges on the host container instance \(similar to the `root` user\)\. This parameter maps to `Privileged` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--privileged` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
 *Required*: no  
*Type*: Boolean  
 *Update requires*: No Interruption 

`JobRoleArn`  
The Amazon Resource Name \(ARN\) of the IAM role that the container can assume for AWS permissions\.  
 *Required*: no  
*Type*: String  
 *Update requires*: No Interruption 

`Environment`  
The environment variables to pass to a container\. This parameter maps to `Env` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--env` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
We do not recommend using plain text environment variables for sensitive information, such as credential data\.
 *Required*: no  
 *Type*: List of [AWS Batch JobDefinition Environment](aws-properties-batch-jobdefinition-environment.md)  
 *Update requires*: No Interruption 

`ReadonlyRootFilesystem`  
When this parameter is true, the container is given read\-only access to its root file system\. This parameter maps to `ReadonlyRootfs` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--read-only` option to `docker run`\.  
 *Required*: no  
*Type*: Boolean  
 *Update requires*: No Interruption 

`Ulimits`  
A list of `ulimits` to set in the container\. This parameter maps to `Ulimits` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--ulimit` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
 *Required*: no  
 *Type*: List of [AWS Batch JobDefinition Ulimit](aws-properties-batch-jobdefinition-ulimit.md)  
 *Update requires*: No Interruption 

`Vcpus`  
The number of vCPUs reserved for the container\. This parameter maps to `CpuShares` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--cpu-shares` option to [docker run](https://docs.docker.com/engine/reference/run/)\. Each vCPU is equivalent to 1,024 CPU shares\.  
 *Required*: yes  
*Type*: Integer  
 *Update requires*: No Interruption 

`Image`  
The image used to start a container\. This string is passed directly to the Docker daemon\. Images in the Docker Hub registry are available by default\. Other repositories are specified with ` repository-url/image:tag `\. Up to 255 letters \(uppercase and lowercase\), numbers, hyphens, underscores, colons, periods, forward slashes, and number signs are allowed\. This parameter maps to `Image` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `IMAGE` parameter of [docker run](https://docs.docker.com/engine/reference/run/)\.  

+ Images in Amazon ECR repositories use the full registry and repository URI \(for example, `012345678910.dkr.ecr.region-name.amazonaws.com/repository-name`\)\. 

+ Images in official repositories on Docker Hub use a single name \(for example, `ubuntu` or `mongo`\)\.

+ Images in other repositories on Docker Hub are qualified with an organization name \(for example, `amazon/amazon-ecs-agent`\)\.

+ Images in other online repositories are qualified further by a domain name \(for example, `quay.io/assemblyline/ubuntu`\)\.
 *Required*: yes  
*Type*: String  
 *Update requires*: No Interruption 