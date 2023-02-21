# AWS::ECS::TaskDefinition MountPoint<a name="aws-properties-ecs-taskdefinition-mountpoint"></a>

The `MountPoint` property specifies details on a volume mount point that is used in a container definition\.

## Syntax<a name="aws-properties-ecs-taskdefinition-mountpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-mountpoint-syntax.json"></a>

```
{
  "[ContainerPath](#cfn-ecs-taskdefinition-mountpoint-containerpath)" : String,
  "[ReadOnly](#cfn-ecs-taskdefinition-mountpoint-readonly)" : Boolean,
  "[SourceVolume](#cfn-ecs-taskdefinition-mountpoint-sourcevolume)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-mountpoint-syntax.yaml"></a>

```
  [ContainerPath](#cfn-ecs-taskdefinition-mountpoint-containerpath): String
  [ReadOnly](#cfn-ecs-taskdefinition-mountpoint-readonly): Boolean
  [SourceVolume](#cfn-ecs-taskdefinition-mountpoint-sourcevolume): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-mountpoint-properties"></a>

`ContainerPath`  <a name="cfn-ecs-taskdefinition-mountpoint-containerpath"></a>
The path on the container to mount the host volume at\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReadOnly`  <a name="cfn-ecs-taskdefinition-mountpoint-readonly"></a>
If this value is `true`, the container has read\-only access to the volume\. If this value is `false`, then the container can write to the volume\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceVolume`  <a name="cfn-ecs-taskdefinition-mountpoint-sourcevolume"></a>
The name of the volume to mount\. Must be a volume name referenced in the `name` parameter of task definition `volume`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)