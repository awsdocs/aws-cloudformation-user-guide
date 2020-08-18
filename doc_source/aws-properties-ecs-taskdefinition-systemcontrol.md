# AWS::ECS::TaskDefinition SystemControl<a name="aws-properties-ecs-taskdefinition-systemcontrol"></a>

A list of namespaced kernel parameters to set in the container\. This parameter maps to `Sysctls` in the [Create a container](https://docs.docker.com/engine/api/v1.35/#operation/ContainerCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `--sysctl` option to [docker run](https://docs.docker.com/engine/reference/run/#security-configuration)\.

It is not recommended that you specify network\-related `systemControls` parameters for multiple containers in a single task that also uses either the `awsvpc` or `host` network mode for the following reasons:
+ For tasks that use the `awsvpc` network mode, if you set `systemControls` for any container, it applies to all containers in the task\. If you set different `systemControls` for multiple containers in a single task, the container that is started last determines which `systemControls` take effect\.
+ For tasks that use the `host` network mode, the `systemControls` parameter applies to the container instance's kernel parameter as well as that of all containers of any tasks running on that container instance\.

## Syntax<a name="aws-properties-ecs-taskdefinition-systemcontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-systemcontrol-syntax.json"></a>

```
{
  "[Namespace](#cfn-ecs-taskdefinition-systemcontrol-namespace)" : String,
  "[Value](#cfn-ecs-taskdefinition-systemcontrol-value)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-systemcontrol-syntax.yaml"></a>

```
  [Namespace](#cfn-ecs-taskdefinition-systemcontrol-namespace): String
  [Value](#cfn-ecs-taskdefinition-systemcontrol-value): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-systemcontrol-properties"></a>

`Namespace`  <a name="cfn-ecs-taskdefinition-systemcontrol-namespace"></a>
The namespaced kernel parameter for which to set a `value`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-ecs-taskdefinition-systemcontrol-value"></a>
The value for the namespaced kernel parameter specified in `namespace`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)