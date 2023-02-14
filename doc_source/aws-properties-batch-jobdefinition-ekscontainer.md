# AWS::Batch::JobDefinition EksContainer<a name="aws-properties-batch-jobdefinition-ekscontainer"></a>

EKS container properties are used in job definitions for Amazon EKS based job definitions to describe the properties for a container node in the pod that's launched as part of a job\. This can't be specified for Amazon ECS based job definitions\.

## Syntax<a name="aws-properties-batch-jobdefinition-ekscontainer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-ekscontainer-syntax.json"></a>

```
{
  "[Args](#cfn-batch-jobdefinition-ekscontainer-args)" : [ String, ... ],
  "[Command](#cfn-batch-jobdefinition-ekscontainer-command)" : [ String, ... ],
  "[Env](#cfn-batch-jobdefinition-ekscontainer-env)" : [ EksContainerEnvironmentVariable, ... ],
  "[Image](#cfn-batch-jobdefinition-ekscontainer-image)" : String,
  "[ImagePullPolicy](#cfn-batch-jobdefinition-ekscontainer-imagepullpolicy)" : String,
  "[Name](#cfn-batch-jobdefinition-ekscontainer-name)" : String,
  "[Resources](#cfn-batch-jobdefinition-ekscontainer-resources)" : Resources,
  "[SecurityContext](#cfn-batch-jobdefinition-ekscontainer-securitycontext)" : SecurityContext,
  "[VolumeMounts](#cfn-batch-jobdefinition-ekscontainer-volumemounts)" : [ EksContainerVolumeMount, ... ]
}
```

### YAML<a name="aws-properties-batch-jobdefinition-ekscontainer-syntax.yaml"></a>

```
  [Args](#cfn-batch-jobdefinition-ekscontainer-args): 
    - String
  [Command](#cfn-batch-jobdefinition-ekscontainer-command): 
    - String
  [Env](#cfn-batch-jobdefinition-ekscontainer-env): 
    - EksContainerEnvironmentVariable
  [Image](#cfn-batch-jobdefinition-ekscontainer-image): String
  [ImagePullPolicy](#cfn-batch-jobdefinition-ekscontainer-imagepullpolicy): String
  [Name](#cfn-batch-jobdefinition-ekscontainer-name): String
  [Resources](#cfn-batch-jobdefinition-ekscontainer-resources): 
    Resources
  [SecurityContext](#cfn-batch-jobdefinition-ekscontainer-securitycontext): 
    SecurityContext
  [VolumeMounts](#cfn-batch-jobdefinition-ekscontainer-volumemounts): 
    - EksContainerVolumeMount
```

## Properties<a name="aws-properties-batch-jobdefinition-ekscontainer-properties"></a>

`Args`  <a name="cfn-batch-jobdefinition-ekscontainer-args"></a>
An array of arguments to the entrypoint\. If this isn't specified, the `CMD` of the container image is used\. This corresponds to the `args` member in the [Entrypoint](https://kubernetes.io/docs/reference/kubernetes-api/workload-resources/pod-v1/#entrypoint) portion of the [Pod](https://kubernetes.io/docs/reference/kubernetes-api/workload-resources/pod-v1/) in Kubernetes\. Environment variable references are expanded using the container's environment\.  
If the referenced environment variable doesn't exist, the reference in the command isn't changed\. For example, if the reference is to "`$(NAME1)`" and the `NAME1` environment variable doesn't exist, the command string will remain "`$(NAME1)`\." `$$` is replaced with `$`, and the resulting string isn't expanded\. For example, `$$(VAR_NAME)` is passed as `$(VAR_NAME)` whether or not the `VAR_NAME` environment variable exists\. For more information, see [CMD](https://docs.docker.com/engine/reference/builder/#cmd) in the *Dockerfile reference* and [Define a command and arguments for a pod](https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Command`  <a name="cfn-batch-jobdefinition-ekscontainer-command"></a>
The entrypoint for the container\. This isn't run within a shell\. If this isn't specified, the `ENTRYPOINT` of the container image is used\. Environment variable references are expanded using the container's environment\.  
If the referenced environment variable doesn't exist, the reference in the command isn't changed\. For example, if the reference is to "`$(NAME1)`" and the `NAME1` environment variable doesn't exist, the command string will remain "`$(NAME1)`\." `$$` is replaced with `$` and the resulting string isn't expanded\. For example, `$$(VAR_NAME)` will be passed as `$(VAR_NAME)` whether or not the `VAR_NAME` environment variable exists\. The entrypoint can't be updated\. For more information, see [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#entrypoint) in the *Dockerfile reference* and [Define a command and arguments for a container](https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/) and [Entrypoint](https://kubernetes.io/docs/reference/kubernetes-api/workload-resources/pod-v1/#entrypoint) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Env`  <a name="cfn-batch-jobdefinition-ekscontainer-env"></a>
The environment variables to pass to a container\.  
Environment variables cannot start with "`AWS_BATCH`"\. This naming convention is reserved for variables that AWS Batch sets\.
*Required*: No  
*Type*: List of [EksContainerEnvironmentVariable](aws-properties-batch-jobdefinition-ekscontainerenvironmentvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Image`  <a name="cfn-batch-jobdefinition-ekscontainer-image"></a>
The Docker image used to start the container\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImagePullPolicy`  <a name="cfn-batch-jobdefinition-ekscontainer-imagepullpolicy"></a>
The image pull policy for the container\. Supported values are `Always`, `IfNotPresent`, and `Never`\. This parameter defaults to `IfNotPresent`\. However, if the `:latest` tag is specified, it defaults to `Always`\. For more information, see [Updating images](https://kubernetes.io/docs/concepts/containers/images/#updating-images) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-batch-jobdefinition-ekscontainer-name"></a>
The name of the container\. If the name isn't specified, the default name "`Default`" is used\. Each container in a pod must have a unique name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Resources`  <a name="cfn-batch-jobdefinition-ekscontainer-resources"></a>
The type and amount of resources to assign to a container\. The supported resources include `memory`, `cpu`, and `nvidia.com/gpu`\. For more information, see [Resource management for pods and containers](https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: [Resources](aws-properties-batch-jobdefinition-ekscontainer-resources.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityContext`  <a name="cfn-batch-jobdefinition-ekscontainer-securitycontext"></a>
The security context for a job\. For more information, see [Configure a security context for a pod or container](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: [SecurityContext](aws-properties-batch-jobdefinition-ekscontainer-securitycontext.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VolumeMounts`  <a name="cfn-batch-jobdefinition-ekscontainer-volumemounts"></a>
The volume mounts for the container\. AWS Batch supports `emptyDir`, `hostPath`, and `secret` volume types\. For more information about volumes and volume mounts in Kubernetes, see [Volumes](https://kubernetes.io/docs/concepts/storage/volumes/) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: List of [EksContainerVolumeMount](aws-properties-batch-jobdefinition-ekscontainervolumemount.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)