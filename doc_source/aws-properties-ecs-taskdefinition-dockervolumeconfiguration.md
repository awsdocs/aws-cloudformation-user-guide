# AWS::ECS::TaskDefinition DockerVolumeConfiguration<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration"></a>

The `DockerVolumeConfiguration` property specifies a Docker volume configuration and is used when you use Docker volumes\. Docker volumes are only supported when you are using the EC2 launch type\. Windows containers only support the use of the `local` driver\. To use bind mounts, specify a `host` instead\.

## Syntax<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-syntax.json"></a>

```
{
  "[Autoprovision](#cfn-ecs-taskdefinition-dockervolumeconfiguration-autoprovision)" : Boolean,
  "[Driver](#cfn-ecs-taskdefinition-dockervolumeconfiguration-driver)" : String,
  "[DriverOpts](#cfn-ecs-taskdefinition-dockervolumeconfiguration-driveropts)" : {Key : Value, ...},
  "[Labels](#cfn-ecs-taskdefinition-dockervolumeconfiguration-labels)" : {Key : Value, ...},
  "[Scope](#cfn-ecs-taskdefinition-dockervolumeconfiguration-scope)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-syntax.yaml"></a>

```
  [Autoprovision](#cfn-ecs-taskdefinition-dockervolumeconfiguration-autoprovision): Boolean
  [Driver](#cfn-ecs-taskdefinition-dockervolumeconfiguration-driver): String
  [DriverOpts](#cfn-ecs-taskdefinition-dockervolumeconfiguration-driveropts): 
    Key : Value
  [Labels](#cfn-ecs-taskdefinition-dockervolumeconfiguration-labels): 
    Key : Value
  [Scope](#cfn-ecs-taskdefinition-dockervolumeconfiguration-scope): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-properties"></a>

`Autoprovision`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-autoprovision"></a>
If this value is `true`, the Docker volume is created if it does not already exist\.  
This field is only used if the `scope` is `shared`\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Driver`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-driver"></a>
The Docker volume driver to use\. The driver value must match the driver name provided by Docker because it is used for task placement\. If the driver was installed using the Docker plugin CLI, use `docker plugin ls` to retrieve the driver name from your container instance\. If the driver was installed using another method, use Docker plugin discovery to retrieve the driver name\. For more information, see [Docker plugin discovery](https://docs.docker.com/engine/extend/plugin_api/#plugin-discovery)\. This parameter maps to `Driver` in the [Create a volume](https://docs.docker.com/engine/api/v1.35/#operation/VolumeCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `xxdriver` option to [docker volume create](https://docs.docker.com/engine/reference/commandline/volume_create/)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DriverOpts`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-driveropts"></a>
A map of Docker driver\-specific options passed through\. This parameter maps to `DriverOpts` in the [Create a volume](https://docs.docker.com/engine/api/v1.35/#operation/VolumeCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `xxopt` option to [docker volume create](https://docs.docker.com/engine/reference/commandline/volume_create/)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Labels`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-labels"></a>
Custom metadata to add to your Docker volume\. This parameter maps to `Labels` in the [Create a volume](https://docs.docker.com/engine/api/v1.35/#operation/VolumeCreate) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.35/) and the `xxlabel` option to [docker volume create](https://docs.docker.com/engine/reference/commandline/volume_create/)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Scope`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-scope"></a>
The scope for the Docker volume that determines its lifecycle\. Docker volumes that are scoped to a `task` are automatically provisioned when the task starts and destroyed when the task stops\. Docker volumes that are scoped as `shared` persist after the task stops\.  
*Required*: No  
*Type*: String  
*Allowed values*: `shared | task`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)