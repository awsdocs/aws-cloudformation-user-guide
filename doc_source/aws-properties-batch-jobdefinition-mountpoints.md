# AWS Batch JobDefinition MountPoints<a name="aws-properties-batch-jobdefinition-mountpoints"></a>

The `MountPoints` property type specifies mount points for data volumes in your container\. This parameter maps to `Volumes` in the [Create a container](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/reference/api/docker_remote_api_v1.19/) and the `--volume` option to [docker run](https://docs.docker.com/engine/reference/run/)\.

## Syntax<a name="aws-properties-batch-jobdefinition-mountpoints-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-mountpoints-syntax.json"></a>

```
{
  "[ReadOnly](#cfn-batch-jobdefinition-mountpoints-readonly)" : Boolean,
  "[SourceVolume](#cfn-batch-jobdefinition-mountpoints-sourcevolume)" : String,
  "[ContainerPath](#cfn-batch-jobdefinition-mountpoints-containerpath)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-mountpoints-syntax.yaml"></a>

```
[ReadOnly](#cfn-batch-jobdefinition-mountpoints-readonly): Boolean
[SourceVolume](#cfn-batch-jobdefinition-mountpoints-sourcevolume): String
[ContainerPath](#cfn-batch-jobdefinition-mountpoints-containerpath): String
```

## Properties<a name="aws-properties-batch-jobdefinition-mountpoints-properties"></a>

`ReadOnly`  <a name="cfn-batch-jobdefinition-mountpoints-readonly"></a>
If this value is `true`, the container has read\-only access to the volume; otherwise, the container can write to the volume\. The default value is `false`\.  
 *Required*: no  
*Type*: Boolean  
 *Update requires*: No Interruption 

`SourceVolume`  <a name="cfn-batch-jobdefinition-mountpoints-sourcevolume"></a>
The name of the volume to mount\.  
 *Required*: no  
*Type*: String  
 *Update requires*: No Interruption 

`ContainerPath`  <a name="cfn-batch-jobdefinition-mountpoints-containerpath"></a>
The path on the container at which to mount the host volume\.  
 *Required*: no  
*Type*: String  
 *Update requires*: No Interruption 