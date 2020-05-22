# AWS::ECS::TaskDefinition HostVolumeProperties<a name="aws-properties-ecs-taskdefinition-volumes-host"></a>

The `HostVolumeProperties` property specifies details on a container instance bind mount host volume\.

## Syntax<a name="aws-properties-ecs-taskdefinition-volumes-host-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-volumes-host-syntax.json"></a>

```
{
  "[SourcePath](#cfn-ecs-taskdefinition-volumes-host-sourcepath)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-volumes-host-syntax.yaml"></a>

```
  [SourcePath](#cfn-ecs-taskdefinition-volumes-host-sourcepath): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-volumes-host-properties"></a>

`SourcePath`  <a name="cfn-ecs-taskdefinition-volumes-host-sourcepath"></a>
When the `host` parameter is used, specify a `sourcePath` to declare the path on the host container instance that is presented to the container\. If this parameter is empty, then the Docker daemon has assigned a host path for you\. If the `host` parameter contains a `sourcePath` file location, then the data volume persists at the specified location on the host container instance until you delete it manually\. If the `sourcePath` value does not exist on the host container instance, the Docker daemon creates it\. If the location does exist, the contents of the source path folder are exported\.  
If you are using the Fargate launch type, the `sourcePath` parameter is not supported\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)