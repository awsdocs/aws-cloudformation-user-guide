# AWS::ECS::TaskDefinition VolumeFrom<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom"></a>

The `VolumeFrom` property specifies details on a data volume from another container in the same task definition\.

## Syntax<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom-syntax.json"></a>

```
{
  "[ReadOnly](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-readonly)" : Boolean,
  "[SourceContainer](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-sourcecontainer)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom-syntax.yaml"></a>

```
  [ReadOnly](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-readonly): Boolean
  [SourceContainer](#cfn-ecs-taskdefinition-containerdefinition-volumesfrom-sourcecontainer): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-containerdefinitions-volumesfrom-properties"></a>

`ReadOnly`  <a name="cfn-ecs-taskdefinition-containerdefinition-volumesfrom-readonly"></a>
If this value is `true`, the container has read\-only access to the volume\. If this value is `false`, then the container can write to the volume\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceContainer`  <a name="cfn-ecs-taskdefinition-containerdefinition-volumesfrom-sourcecontainer"></a>
The name of another container within the same task definition from which to mount volumes\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)