# Amazon ECS TaskDefinition DockerVolumeConfiguration<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration"></a>

<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-description"></a>The `DockerVolumeConfiguration` property type specifies the configuration of a Docker volume\. This parameter is specified when using Docker volumes\. Docker volumes are only supported when using the EC2 launch type\. Windows containers only support the use of the `local` driver\. To use bind mounts, specify a `host` instead\.

<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-inheritance"></a> `DockerVolumeConfiguration` is a property of the [Amazon Elastic Container Service TaskDefinition Volumes](aws-properties-ecs-taskdefinition-volumes.md) property type\.

## Syntax<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-syntax.json"></a>

```
{
  "[Autoprovision](#cfn-ecs-taskdefinition-dockervolumeconfiguration-autoprovision)" : Boolean,
  "[Driver](#cfn-ecs-taskdefinition-dockervolumeconfiguration-driver)" : String,
  "[DriverOpts](#cfn-ecs-taskdefinition-dockervolumeconfiguration-driveropts)" : [ String, ... ] ,
  "[Labels](#cfn-ecs-taskdefinition-dockervolumeconfiguration-labels)" : [ String, ... ] ,
  "[Scope](#cfn-ecs-taskdefinition-dockervolumeconfiguration-scope)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-syntax.yaml"></a>

```
[Autoprovision](#cfn-ecs-taskdefinition-dockervolumeconfiguration-autoprovision): Boolean
[Driver](#cfn-ecs-taskdefinition-dockervolumeconfiguration-driver): String
[DriverOpts](#cfn-ecs-taskdefinition-dockervolumeconfiguration-driveropts)
  - String
[Labels](#cfn-ecs-taskdefinition-dockervolumeconfiguration-labels)
  - String
[Scope](#cfn-ecs-taskdefinition-dockervolumeconfiguration-scope): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-properties"></a>

`Autoprovision`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-autoprovision"></a>
If `true`, the Docker volume is created if it does not already exist\. This field is only used if the scope is `shared`\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Driver`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-driver"></a>
The Docker volume driver to use\. The driver value must match the driver name provided by Docker because it is used for task placement\. For more information, see [DockerVolumeConfiguration](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DockerVolumeConfiguration.html) in the *Amazon Elastic Container Service API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DriverOpts`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-driveropts"></a>
A map of Docker driver specific options passed through\. For more information, see [DockerVolumeConfiguration](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DockerVolumeConfiguration.html) in the *Amazon Elastic Container Service API Reference*\.  
Duplicate values are not allowed\.  
 *Required*: No  
 *Type*: List of Strings  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Labels`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-labels"></a>
Custom metadata to add to your Docker volume\. For more information, see [DockerVolumeConfiguration](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DockerVolumeConfiguration.html) in the *Amazon Elastic Container Service API Reference*\.  
Duplicate values are not allowed\.  
 *Required*: No  
 *Type*: List of String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Scope`  <a name="cfn-ecs-taskdefinition-dockervolumeconfiguration-scope"></a>
The scope for the Docker volume which determines it's lifecycle\. Docker volumes that are scoped to a `task` are automatically provisioned when the task starts and destroyed when the task stops\. Docker volumes that are scoped as `shared` persist after the task stops\.  
Valid values include `shared` and `task`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-ecs-taskdefinition-dockervolumeconfiguration-seealso"></a>
+ [DockerVolumeConfiguration](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_DockerVolumeConfiguration.html) in the *Amazon Elastic Container Service API Reference*