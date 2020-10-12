# AWS::ECS::TaskDefinition Volume<a name="aws-properties-ecs-taskdefinition-volumes"></a>

The `Volume` property specifies a data volume used in a task definition\. For tasks that use a Docker volume, specify a `DockerVolumeConfiguration`\. For tasks that use a bind mount host volume, specify a `host` and optional `sourcePath`\. For more information, see [Using Data Volumes in Tasks](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_data_volumes.html)\.

## Syntax<a name="aws-properties-ecs-taskdefinition-volumes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-volumes-syntax.json"></a>

```
{
  "[DockerVolumeConfiguration](#cfn-ecs-taskdefinition-volume-dockervolumeconfiguration)" : DockerVolumeConfiguration,
  "[EFSVolumeConfiguration](#cfn-ecs-taskdefinition-volume-efsvolumeconfiguration)" : EFSVolumeConfiguration,
  "[Host](#cfn-ecs-taskdefinition-volumes-host)" : HostVolumeProperties,
  "[Name](#cfn-ecs-taskdefinition-volumes-name)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-volumes-syntax.yaml"></a>

```
  [DockerVolumeConfiguration](#cfn-ecs-taskdefinition-volume-dockervolumeconfiguration): 
    DockerVolumeConfiguration
  [EFSVolumeConfiguration](#cfn-ecs-taskdefinition-volume-efsvolumeconfiguration): 
    EFSVolumeConfiguration
  [Host](#cfn-ecs-taskdefinition-volumes-host): 
    HostVolumeProperties
  [Name](#cfn-ecs-taskdefinition-volumes-name): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-volumes-properties"></a>

`DockerVolumeConfiguration`  <a name="cfn-ecs-taskdefinition-volume-dockervolumeconfiguration"></a>
This parameter is specified when you are using Docker volumes\. Docker volumes are only supported when you are using the EC2 launch type\. Windows containers only support the use of the `local` driver\. To use bind mounts, specify the `host` parameter instead\.  
*Required*: No  
*Type*: [DockerVolumeConfiguration](aws-properties-ecs-taskdefinition-dockervolumeconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EFSVolumeConfiguration`  <a name="cfn-ecs-taskdefinition-volume-efsvolumeconfiguration"></a>
This parameter is specified when you are using an Amazon Elastic File System file system for task storage\.  
*Required*: No  
*Type*: [EFSVolumeConfiguration](aws-properties-ecs-taskdefinition-efsvolumeconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Host`  <a name="cfn-ecs-taskdefinition-volumes-host"></a>
This parameter is specified when you are using bind mount host volumes\. The contents of the `host` parameter determine whether your bind mount host volume persists on the host container instance and where it is stored\. If the `host` parameter is empty, then the Docker daemon assigns a host path for your data volume\. However, the data is not guaranteed to persist after the containers associated with it stop running\.  
Windows containers can mount whole directories on the same drive as `$env:ProgramData`\. Windows containers cannot mount directories on a different drive, and mount point cannot be across drives\. For example, you can mount `C:\my\path:C:\my\path` and `D:\:D:\`, but not `D:\my\path:C:\my\path` or `D:\:C:\my\path`\.  
*Required*: No  
*Type*: [HostVolumeProperties](aws-properties-ecs-taskdefinition-volumes-host.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-ecs-taskdefinition-volumes-name"></a>
The name of the volume\. Up to 255 letters \(uppercase and lowercase\), numbers, and hyphens are allowed\. This name is referenced in the `sourceVolume` parameter of container definition `mountPoints`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)